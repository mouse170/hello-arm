ifneq ($(KERNELRELEASE),)
	obj-m := hello1.o
else
	KDIR := /lib/modules/$(shell uname -r)/build
all:
	make -C $(KDIR) M=$(shell pwd) modules
clean:
	rm -f *.ko *.o *.mod.o *.mod.c *.symvers
endif
