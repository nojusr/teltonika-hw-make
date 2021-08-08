CFLAGS:=-Wall -fPIC
CPPFLAGS:=-I$(PWD)
LDFLAGS:=-shared

SRC:=$(wildcard *.c)
OBJ:=$(SRC:.c=.o)

BIN=libmathfunctions.so

.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJ)
	$(CC) $(CFLAGS) $(CPPFLAGS) $(LDFLAGS) -o $(BIN) $(OBJ)

clean:
	$(RM) $(BIN) $(OBJ)