CC := gcc
CFLAGS := -g
LD_FLAGS =

EXECUTABLE := Example
SOURCES := $(wildcard **/*.c)
OBJECTS := $(SOURCES:.c=.o)
DELETE_EXEC :=rm -rf

ifeq ($(OS), Windows_NT)
ifndef TERM
DELETE_EXEC := del /Q
endif
endif

NIXSLASHES := ../moo ../rawr
ifeq ($(OS), Windows_NT)
WINSLASHES := $(subst /,\,$(NIXSLASHES))
endif


all: $(EXECUTABLE).exe

$(EXECUTABLE).exe: $(OBJECTS)
	$(CC) $(LD_FLAGS) $(OBJECTS) -o $@

slashes:
	@echo $(NIXSLASHES)
	@echo $(WINSLASHES)

clean:
	$(DELETE_EXEC) $(OBJECTS) $(EXECUTABLE).exe
