# 
# Liviu Caramida (carliv@xda), Carliv Image Kitchen source
#
MAKEFLAGS += --silent
CC = gcc10
AR = ar -rcs
RM = rm -f
CFLAGS = -std=c99 -pipe
LIB = libcutils.a
LIB_OBJS = config_utils.o fs_config.o hashmap.o

all: $(LIB) lib

clean:
	$(RM) $(LIB_OBJS) $(LIB)

$(LIB): $(LIB_OBJS)

%.o:%.c $(LIB_OBJS)
	$(CC) $(CFLAGS) -o $@ $^

lib:
	$(AR) $(LIB) $(LIB_OBJS)

.PHONY: all clean
