BASE=../../../../..

IKS_DIR=$(BASE)/libs/iksemel
IKS_LA=$(IKS_DIR)/src/libiksemel.la
LOCAL_OBJS= main.o ../srgs.o
LOCAL_SOURCES= main.c
LOCAL_CFLAGS += -I../ -I$(BASE)/libs/iksemel/include $(PCRE_CFLAGS)
LOCAL_LIBADD += $(IKS_LA) $(PCRE_LIBS)
include $(BASE)/build/modmake.rules

$(IKS_LA): $(IKS_DIR) $(IKS_DIR)/.update
	@cd $(IKS_DIR) && $(MAKE)
	@$(TOUCH_TARGET)

local_all:
	libtool --mode=link gcc main.o ../srgs.o -o test test_srgs.la

local_clean:
	-rm test
