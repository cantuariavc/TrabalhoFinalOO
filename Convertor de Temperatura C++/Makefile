# Executavel
BINFOLDER := bin/
# .hpp
INCFOLDER := inc/
# .cpp
SRCFOLDER := src/
# .o
OBJFOLDER := obj/

CC := g++

CFLAGS := -W -Wall -ansi -pedantic

SRCFILES := $(wildcard src/*.cpp)

all: 	$(SRCFILES:src/%.cpp=obj/%.o)
	$(CC) $(CFLAGS) obj/*.o -o bin/main.out

obj/%.o:src/%.cpp
	$(CC) $(CFLAGS) -c $< -o $@ -I./inc

run:	bin/main.out
	bin/main.out

.PHONY: clean
clean:
	rm -rf obj/*
	rm -rf bin/*
