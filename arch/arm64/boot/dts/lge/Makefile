ifeq ($(CONFIG_MACH_MSM8996_LUCYE_KR),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_GLOBAL_COM),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_GLOBAL_CA),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_VZW),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_SPR_US),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_NAO_US),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_ATT_US),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_TMO_US),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_CLR_PR),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_GLOBAL_LDU),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_LGU_LDU),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ifeq ($(CONFIG_MACH_MSM8996_LUCYE_ACG_US),y)
DTS_TARGET := msm8996-lucye_global_com
endif

ALL_DTS := $(notdir $(wildcard echo $(srctree)/$(src)/$(DTS_TARGET)/*.dts))
dtb-y += $(patsubst %.dts,%.dtb,$(ALL_DTS))

DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif

always  := $(addprefix ../,$(DTB_LIST))

$(obj)/../%.dtb: $(src)/$(DTS_TARGET)/%.dts FORCE
	$(call if_changed_dep,dtc)

clean-files := *.dtb
