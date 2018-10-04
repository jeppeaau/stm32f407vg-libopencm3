######################################################################
#  Project
######################################################################

BINARY		= miniblink
SRCFILES	= miniblink.c
OPENCM3_DIR = ../libopencm3
STFLASH = $(shell which st-flash)

DEVICE=STM32F407VG
all: elf bin

include ../Makefile.incl

# Flash 64k Device
flash:	$(BINARY).bin
	$(STFLASH) $(FLASHSIZE) write $(BINARY).bin 0x8000000

# Flash 128k Device
bigflash: $(BINARY).bin
	$(STFLASH) --flash=128k write $(BINARY).bin 0x8000000
# End
