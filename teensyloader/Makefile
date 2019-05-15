##############################################
# Author: alzhao@gmail.com
#
##############################################

include $(TOPDIR)/rules.mk

PKG_NAME:=teensyloader
PKG_VERSION=2.1
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=http://github.com/PaulStoffregen/teensy_loader_cli
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=ee411ad7caa2b40751f1b776c3311320777a9609
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/teensyloader
	SECTION:=base
	CATEGORY:=Network
	TITLE:=teensyloader
	DEPENDS:=+libusb-compat
endef

define Package/teensyloader/description
	teensloader
endef

define Package/teensyloader/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/teensy_loader_cli $(1)/usr/bin/
endef

$(eval $(call BuildPackage,teensyloader))
