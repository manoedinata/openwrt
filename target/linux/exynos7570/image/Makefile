# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/image.mk

# S-BOOT only takes an Android boot image; for now the kernel and dtb are
# wrapped into one outside the build (mainline-tools/pack.sh, uniLoader).
define Device/Default
  PROFILES := Default
  KERNEL_NAME := Image
  KERNEL := kernel-bin
  DEVICE_DTS_DIR := $(DTS_DIR)/exynos
  IMAGES :=
endef

define Device/samsung_j4lte
  DEVICE_VENDOR := Samsung
  DEVICE_MODEL := Galaxy J4
  DEVICE_VARIANT := SM-J400F
  SOC := exynos7570
  DEVICE_DTS := exynos7570-j4lte
  # mobile data (feed j4: samsungipcd, ModemManager with its plugin)
  DEVICE_PACKAGES := samsungipcd modemmanager luci-proto-modemmanager \
	luci-theme-material
endef
TARGET_DEVICES += samsung_j4lte

$(eval $(call BuildImage))
