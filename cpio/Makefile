# 
# Liviu Caramida (carliv@xda), Carliv Image Kitchen source
#
MAKEFLAGS += --silent
OUT = ../out
CC=gcc10
CFLAGS = -std=c99 -pipe

RM = rm -f
CP = cp

all: mkbootfs

mkbootfs:
	$(CC) $@.c -o $@
	strip $@
	$(CP) $@ $(OUT)

clean:
	$(RM) mkbootfs

.PHONY: all clean
