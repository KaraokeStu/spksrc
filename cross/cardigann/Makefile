PKG_NAME = cardigann
PKG_VERS = 1.9.3
PKG_EXT = tar.gz
PKG_DIR = 
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
HOMEPAGE = https://github.com/cardigann/cardigann
COMMENT  = A proxy server for adding new indexers to Sonarr, SickRage and other media managers
LICENSE  = MIT

DEPENDS = native/go

CONFIGURE_TARGET = nop
COMPILE_TARGET = nop

# Define CARDIGAN_ARCH based on our architechture
ifeq ($(findstring $(ARCH),88f5281 88f6281 alpine armada370 armada375 armada38x armadaxp comcerto2k monaco),$(ARCH))
PKG_DIST_NAME = cardigann-1.9.3-linux-arm.tar.gz
PKG_DIST_SITE = https://bin.equinox.io/a/i1Zb3wkLEqP
endif
ifeq ($(findstring $(ARCH),evansport),$(ARCH))
PKG_DIST_NAME = cardigann-1.9.3-linux-386.tar.gz
PKG_DIST_SITE = https://bin.equinox.io/a/hd2Jwjw9U5f
endif
ifeq ($(findstring $(ARCH),avoton braswell bromolow cedarview x86 x64),$(ARCH))
PKG_DIST_NAME = cardigann-1.9.3-linux-amd64.tar.gz
PKG_DIST_SITE = https://bin.equinox.io/a/4vpjNf1aFuV
endif
ifeq ($(PKG_DIST_NAME),)
$(error Unsupported ARCH $(ARCH))
endif

include ../../mk/spksrc.cross-cc.mk
