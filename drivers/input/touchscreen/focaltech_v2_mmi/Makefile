# Makefile for the focaltech touchscreen drivers.

ifneq ($(filter m y,$(CONFIG_INPUT_TOUCHSCREEN_MMI)),)
	ccflags-y += -DCONFIG_INPUT_TOUCHSCREEN_MMI
endif
ifneq ($(filter m y,$(CONFIG_TOUCHSCREEN_FTS_V2_MMI_ENABLE_DOUBLE_TAP)),)
	EXTRA_CFLAGS += -DFOCALTECH_SENSOR_EN
endif
ifneq ($(filter m y,$(CONFIG_TOUCHSCREEN_FTS_V2_MMI_ENABLE_PALM)),)
	EXTRA_CFLAGS += -DFOCALTECH_PALM_SENSOR_EN
endif
ifneq ($(filter m y,$(CONFIG_TOUCHSCREEN_FTS_V2_MMI_PEN_NOTIFIER)),)
	EXTRA_CFLAGS += -DFOCALTECH_PEN_NOTIFIER
endif

ifneq ($(filter m y, $(CONFIG_DRM_PANEL_NOTIFICATIONS)),)
	EXTRA_CFLAGS += -DCONFIG_DRM_PANEL_NOTIFICATIONS
endif

obj-$(CONFIG_TOUCHSCREEN_FTS_V2_MMI) += focaltech_v2_mmi.o

focaltech_v2_mmi-y += focaltech_core.o focaltech_ex_fun.o focaltech_ex_mode.o \
	focaltech_gesture.o focaltech_esdcheck.o focaltech_point_report_check.o \
	focaltech_i2c.o focaltech_flash.o focaltech_ts_mmi.o \
	focaltech_flash/focaltech_upgrade_ft3518u.o \
	focaltech_flash/focaltech_upgrade_ft5452i.o
