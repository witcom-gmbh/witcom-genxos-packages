include $(TOPDIR)/rules.mk

PKG_NAME:=witcom-genxos-helper
PKG_VERSION:=2022.06.10
PKG_RELEASE:=1

PKG_MAINTAINER:=Carsten Buchberger <c.buchberger@witcom.de>
PKG_LICENSE:=Apache-2.0

include $(INCLUDE_DIR)/package.mk

Build/Compile=

define Package/witcom-genxos-helper/Default
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=WiTCOM GenXOS helper utilities
#  PKGARCH:=all
endef

define Package/witcom-genxos-helper
  $(call Package/witcom-genxos-helper/Default)
endef

define Package/witcom-genxos-helper/description
	Provides some helper scripts for GenXOS based devices
endef

define Package/witcom-genxos-helper/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) ./files/usr/bin/getfirstlanport.lua $(1)/usr/bin/getfirstlanport.lua
	$(INSTALL_BIN) ./files/usr/bin/getfirstlanport $(1)/usr/bin/getfirstlanport
endef

$(eval $(call BuildPackage,witcom-genxos-helper))
