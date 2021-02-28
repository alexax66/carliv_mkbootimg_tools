#
# Liviu Caramida (carliv@xda), Carliv Image Kitchen source
#
MAKEFLAGS += --silent
CC = gcc10
AR = ar -rcs
RM = rm -f
CFLAGS = -std=c99 -pipe
LIB = libmincrypt.a
LIB_OBJS = dsa_sig.o p256.o p256_ec.o p256_ecdsa.o rsa.o sha.o sha256.o

all: $(LIB) lib

clean:
	$(RM) $(LIB_OBJS) $(LIB)

$(LIB): $(LIB_OBJS)

%.o: %.c $(LIB_OBJS)
	$(CC) $(CFLAGS) -o $@ $^

lib:
	$(AR) $(LIB) $(LIB_OBJS)

O.PHONY: all clean
