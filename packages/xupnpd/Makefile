#
# Copyright (C) 2011-2014 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

all: .done

.done:
	patch -d $(TOP) -p3 -i $(CURDIR)/fix-path.patch
	rm -f ../../../openwrt_trunk/feeds/packages/multimedia/xupnpd/patches/100-default_config.patch
	rm -f ../../../openwrt_trunk/feeds/packages/multimedia/xupnpd/patches/101-root_dir_param.patch
	cp -f ./S94xupnpd ../../../openwrt_trunk/feeds/packages/multimedia/xupnpd/files/
	cp -f ./5*.patch ../../../openwrt_trunk/feeds/packages/multimedia/xupnpd/patches/
	@touch $@

clean:
	@rm -f .done

.PHONY: clean
