-include ../tools.mk

# Apparently older versions of GCC segfault if -g is passed...
CC := $(CC:-g=)

all:
	$(RUSTC) foo.rs -C lto
	$(CC) bar.c -lfoo -o $(call RUN_BINFILE,bar) $(EXTRACFLAGS) -lstdc++
	$(call RUN,bar)
