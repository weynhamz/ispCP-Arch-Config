#!/usr/bin/make -f

# ispCP ω (OMEGA) a Virtual Hosting Control Panel
# Copyright (C) 2001-2006 by moleSoftware GmbH - http://www.molesoftware.com
# Copyright (C) 2006-2010 by isp Control Panel - http://ispcp.net
#
# Version: $Id: Makefile 2505 2010-01-06 20:30:53Z nuxwin $
#
# The contents of this file are subject to the Mozilla Public License
# Version 1.1 (the "License"); you may not use this file except in
# compliance with the License. You may obtain a copy of the License at
# http://www.mozilla.org/MPL/
#
# Software distributed under the License is distributed on an "AS IS"
# basis, WITHOUT WARRANTY OF ANY KIND, either express or implied. See the
# License for the specific language governing rights and limitations
# under the License.
#
# The Original Code is "VHCS - Virtual Hosting Control System".
#
# The Initial Developer of the Original Code is moleSoftware GmbH.
# Portions created by Initial Developer are Copyright (C) 2001-2006
# by moleSoftware GmbH. All Rights Reserved.
# Portions created by the ispCP Team are Copyright (C) 2006-2010 by
# isp Control Panel. All Rights Reserved.
#
# The ispCP ω Home Page is:
#
#    http://isp-control.net
#

export

install:
	if test $(HOST_OS) = arch ; then \
		cp ./ispcp.conf $(SYSTEM_CONF) ; \
		(cd ./fcgi      && $(MAKE) install &); \
		(cd ./bind      && $(MAKE) install &); \
		(cd ./rc.d      && $(MAKE) install &); \
		(cd ./conf.d    && $(MAKE) install &); \
		(cd ./cron.d    && $(MAKE) install &); \
		(cd ./apache    && $(MAKE) install &); \
		(cd ./awstats   && $(MAKE) install &); \
		(cd ./postfix   && $(MAKE) install &); \
		(cd ./courier   && $(MAKE) install &); \
		(cd ./proftpd   && $(MAKE) install &); \
		(cd ./logrotate && $(MAKE) install &); \
	fi

uninstall:
	if test $(HOST_OS) = arch ; then \
		rm -rf $(SYSTEM_CONF)/ispcp.conf ;  \
		(cd ./fcgi      && $(MAKE) install &); \
		(cd ./bind      && $(MAKE) uninstall &); \
		(cd ./rc.d      && $(MAKE) uninstall &); \
		(cd ./conf.d    && $(MAKE) uninstall &); \
		(cd ./cron.d    && $(MAKE) uninstall &); \
		(cd ./apache    && $(MAKE) uninstall &); \
		(cd ./awstats   && $(MAKE) uninstall &); \
		(cd ./postfix   && $(MAKE) uninstall &); \
		(cd ./courier   && $(MAKE) uninstall &); \
		(cd ./proftpd   && $(MAKE) uninstall &); \
		(cd ./logrotate && $(MAKE) uninstall &); \
	fi
