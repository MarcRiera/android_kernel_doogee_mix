ccflags-y += -I$(srctree)/drivers/misc/mediatek/pmic
ccflags-y += -I$(srctree)/drivers/misc/mediatek/pmic_wrap/$(CONFIG_MTK_PLATFORM)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/include/spm_v2/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/$(CONFIG_MTK_PLATFORM)

ifeq ($(CONFIG_MTK_TINYSYS_SSPM_SUPPORT), y)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sspm/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sspm/$(MTK_PLATFORM)/
obj-y += pmic_ipi.o
endif

ifeq ($(CONFIG_MTK_GAUGE_VERSION),30)
obj-$(CONFIG_MTK_SMART_BATTERY) += mtk_battery_hal.o pmic_timer_service.o
endif

obj-$(CONFIG_MTK_PMIC_CHIP_MT6355)	+= pmic.o pmic_irq.o pmic_common.o \
		pmic_api.o pmic_lp_api.o \
		regulator_codegen.o pmic_auxadc.o \
		pmic_initial_setting.o \
		pmic_throttling_dlpt.o pmic_debugfs.o pmic_bif.o
