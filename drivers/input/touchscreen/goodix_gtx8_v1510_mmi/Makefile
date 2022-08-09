ifneq ($(filter m y,$(CONFIG_INPUT_TOUCHSCREEN_MMI)),)
	ccflags-y += -DCONFIG_INPUT_TOUCHSCREEN_MMI
endif

goodix_v1510_mmi-y += goodix_ts_i2c.o goodix_ts_core.o goodix_ts_test.o goodix_cfg_bin.o goodix_gtx8_update.o goodix_ts_gesture.o goodix_ts_tools.o goodix_ts_mmi.o
obj-$(CONFIG_TOUCHSCREEN_GOODIX_GTX8_MMI) += goodix_v1510_mmi.o
