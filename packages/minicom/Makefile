#
# Copyright (C) 2011-2014 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

all: .done

.done:
	patch -d $(TOP) -p3 -i $(CURDIR)/fix-path.patch
	rm -f ../../../openwrt_trunk/feeds/packages/utils/minicom/patches/010-resolve-getline-conflict.patch
	cp -f ./500-entware-path.patch ../../../openwrt_trunk/feeds/packages/utils/minicom/patches/
	@touch $@

clean:
	@rm -f .done

.PHONY: clean
