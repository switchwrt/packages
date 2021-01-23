include $(TOPDIR)/rules.mk

PKG_NAME := libteam
PKG_FIXUP := autoreconf
PKG_BUILD_DEPENDS := libdaemon jansson
PKG_INSTALL := 1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL=https://github.com/jpirko/libteam.git
PKG_SOURCE_DATE:=2021-01-18
PKG_SOURCE_VERSION:=267f24839536234ca621d4fd0466d3b57cb6dccd

PKG_LICENSE:=LGPL-2.1

include $(INCLUDE_DIR)/package.mk

define Package/libteam
  SECTION := base
  CATEGORY := Network
  DEPENDS := +libnl +libnl-cli +libnl-core +libnl-genl +libnl-nf +libnl-route +libdaemon +jansson
  TITLE := Library for controlling team network device
  URL := http://libteam.org/
endef

define Package/libteam/install
	$(INSTALL_DIR) $(1)/
	$(CP) $(PKG_INSTALL_DIR)/. $(1)/
endef

$(eval $(call BuildPackage,libteam))
