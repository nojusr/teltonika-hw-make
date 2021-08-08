CFLAGS:=-Wall
CPPFLAGS:=-I$(PWD)
LDFLAGS:=

#varnames could use a bit of work
LIBOBJ=file_reader.o
LIBBIN=libfilereader.so

OBJ:=main.o
BIN=main

.PHONY: all lib prog clean

all: lib prog

lib: $(LIBBIN)

prog: $(BIN)

$(LIBBIN): $(LIBOBJ)
	$(CC) $(CFLAGS) -fPIC $(CPPFLAGS) -shared -o $@ $^ $(LDFLAGS)

$(BIN): $(OBJ)
	$(CC) $(CPPFLAGS) -o $@ $^ $(LDFLAGS) -L./ -lfilereader

clean:
	$(RM) $(LIBBIN) $(LIBOBJ) $(BIN) $(OBJ)