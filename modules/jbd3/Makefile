# SPDX-License-Identifier: GPL-2.0-only
#
# Makefile for the linux journaling routines.
#

#obj-$(CONFIG_JBD2) += jbd3.o
#obj-m += jbd3.o
obj-m := jbd3.o

#jbd3-objs := transaction.o commit.o recovery.o checkpoint.o revoke.o journal.o
jbd3-y := transaction.o commit.o recovery.o checkpoint.o revoke.o journal.o

KDIR := /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

clean:
	rm *.ko
	rm *.o
	rm *.mod.*
