SPK_NAME = cardigann
SPK_VERS = 1.9.3
SPK_REV = 1
SPK_ICON = src/cardigann.png

DEPENDS  = cross/$(SPK_NAME)
SPK_DEPENDS = 

MAINTAINER = KaraokeStu
DESCRIPTION = A server for adding extra indexers to Sonarr, SickRage and CouchPotato via Torznab and TorrentPotato proxies. Behind the scenes Cardigann logs in and runs searches and then transforms the results into a compatible format.
ADMIN_PORT = 5060
RELOAD_UI = yes
DISPLAY_NAME = Cardigann
CHANGELOG = "Initial version at 1.9.3"

HOMEPAGE   = https://github.com/cardigann/cardigann
LICENSE    = MIT

SSS_SCRIPT       = src/dsm-control.sh
FWPORTS          = src/${SPK_NAME}.sc

INSTALL_PREFIX = /usr/local/$(SPK_NAME)

POST_STRIP_TARGET = cardigann_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: cardigann_extra_install
cardigann_extra_install:
	install -m 755 -d $(STAGING_DIR)/app
	install -m 755 -d $(STAGING_DIR)/app/images
	for size in 16 24 32 48 72; do \
		convert $(SPK_ICON) -thumbnail $${size}x$${size} \
		        $(STAGING_DIR)/app/images/$(SPK_NAME)-$${size}.png ; \
	done
	
