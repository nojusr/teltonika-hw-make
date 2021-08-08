CFLAGS:=-Wall
CPPFLAGS:=-I$(PWD)

SRC:=$(wildcard *.c)
OBJ:=$(SRC:.c=.o)

BIN:=calculator

.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJ)
	$(CC) $(CFLAGS) -o $@ $^

clean:
	$(RM) $(BIN) $(OBJ)
