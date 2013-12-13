BASE=../../../..

IKS_DIR=$(BASE)/libs/iksemel
IKS_LA=$(IKS_DIR)/src/libiksemel.la
LOCAL_CFLAGS += -I$(BASE)/libs/iksemel/include $(PCRE_CFLAGS)
LOCAL_LIBADD += $(IKS_LA) $(PCRE_LIBS)
LOCAL_OBJS=  \
	iks_helpers.o \
	nlsml.o \
	rayo_components.o \
	rayo_cpa_component.o \
	rayo_cpa_detector.o \
	rayo_elements.o \
	rayo_fax_components.o \
	rayo_input_component.o \
	rayo_output_component.o \
	rayo_prompt_component.o \
	rayo_record_component.o \
	sasl.o \
	srgs.o \
	xmpp_streams.o
LOCAL_SOURCES=	\
	iks_helpers.c \
	nlsml.c \
	rayo_components.c \
	rayo_cpa_component.c \
	rayo_cpa_detector.c \
	rayo_elements.c \
	rayo_fax_components.c \
	rayo_input_component.c \
	rayo_output_component.c \
	rayo_prompt_component.c \
	rayo_record_component.c \
	sasl.c \
	srgs.c \
	xmpp_streams.c
include $(BASE)/build/modmake.rules

$(IKS_LA): $(IKS_DIR) $(IKS_DIR)/.update
	@cd $(IKS_DIR) && $(MAKE)
	@$(TOUCH_TARGET)
