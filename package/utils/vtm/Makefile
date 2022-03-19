include $(TOPDIR)/rules.mk
PKG_NAME:=vtm
PKG_VERSION:=0.6.0
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/netxs-group/vtm/tar.gz/refs/tags/v$(PKG_VERSION)?
PKG_HASH:=b572a7f7f4b1271faf6dac5c0f91505b878eee1cfcbcca4a9323b97e9325e16b

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/vtm
	SECTION:=utils
	CATEGORY:=Utilities
	SUBMENU:=Terminal
	TITLE:=Monotty Desktopio
	URL:=https://vtm.netxs.online/
	PKG_DEFAULT_DEPENDS:=
endef

define Package/vtm/description
	Terminal multiplexer with window manager and session sharing.
endef

CMAKE_SOURCE_SUBDIR:=src
TARGET_LDFLAGS:=

define Package/vtm/install
	$(INSTALL_DIR) $(1)/opt/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/opt/bin/vtm $(1)/opt/bin
endef
$(eval $(call BuildPackage,vtm))
