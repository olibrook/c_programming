CC = c99 -ggdb
#List all 'c' files by wildcard.
SOURCES=$(wildcard *.c)
#Get the 'exe' equivalent of said file
EXECUTABLES=$(SOURCES:%.c=%)

all: $(EXECUTABLES)
.PHONY: all
$(EXECUTABLES): % : %.c
	$(CC) $< -o $@ 

.PHONY clean:
clean:
	find ./ -type f -executable -delete 

.PHONY cores:
cores:
	find ./ -type f -name "core.*" -delete


rebuild: cores clean all
