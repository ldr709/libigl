.PHONY: all

all: example

# Shared flags etc.
include ../Makefile.conf

.PHONY: example

CFLAGS+=-g -Wall 
inc=$(LIBIGL_INC)
lib=$(LIBIGL_LIB)

example: example.o
	g++ $(CFLAGS) -o example example.o $(lib) 

example.o: example.cpp
	g++ $(CFLAGS) $(deps) -c example.cpp -o example.o $(inc)
clean:
	rm -f example.o
	rm -f example
