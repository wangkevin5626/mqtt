.PHONY: all
DEPENDS     := -D../platform/os/arm-linux
CC          := gcc

CFLAGS      := -I../include
CFLAGS      += -I../include/iot-sdk
CFLAGS      += -I../include/mbedtls

LDFLAGS     := -L../lib
LDFLAGS     += -L../lib/libiot_sdk.a -L../lib/libiot_platform.a
LDFLAGS     += -Bstatic -L../lib/libiot_sdk.a
LDFLAGS     += -lgcov

all ::
	$(CC) $(CFLAGS) -o ext.mqtt mqtt-example.c $(LDFLAGS) $(LDFLAGS)

clean ::
	rm -vf ext.mqtt

