LDFLAGS = 
CFLAGS = -g -Wall -Wextra -std=c99
CC = clang

OBJS = lee.o maze.o mazeio.o


# Assuming your main is in solvemaze.c:

all: solvemaze

solvemaze: solvemaze.o $(OBJS)
	$(CC) $(LDFLAGS) -o $@ $^

%.o: %.c
	$(CC) $(CFLAGS) -MMD -c -o $@ $<

# deps made thanks to -MMD above, just include them
-include $(SOURCES:.c=.d)

clean:
	rm -f *.o *.d *~

