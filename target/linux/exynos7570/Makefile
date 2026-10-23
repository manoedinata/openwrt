# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

ARCH:=aarch64
BOARD:=exynos7570
BOARDNAME:=Samsung Exynos7570
FEATURES:=fpu usb rtc ext4 targz
CPU_TYPE:=cortex-a53

KERNEL_PATCHVER:=6.12

include $(INCLUDE_DIR)/target.mk

KERNELNAME:=Image dtbs

DEFAULT_PACKAGES += e2fsprogs luci

$(eval $(call BuildTarget))
