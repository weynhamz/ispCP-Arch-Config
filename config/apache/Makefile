#!/usr/bin/make -f

# ispCP ω (OMEGA) a Virtual Hosting Control Panel
# Copyright (C) 2001-2006 by moleSoftware GmbH - http://www.molesoftware.com
# Copyright (C) 2006-2009 by isp Control Panel - http://ispcp.net
#
# Version: $Id: Makefile 2268 2009-12-05 12:15:49Z nuxwin $
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
# Portions created by the ispCP Team are Copyright (C) 2006-2009 by
# isp Control Panel. All Rights Reserved.
#
# The ispCP ω Home Page is:
#
#    http://isp-control.net
#

ROOT_APACHE_CONF=$(ROOT_CONF)/httpd

export

install:

	$(SYSTEM_MAKE_DIRS) $(ROOT_APACHE_CONF)
	$(SYSTEM_MAKE_DIRS) $(ROOT_APACHE_CONF)/conf/extra/httpd-mods
	$(SYSTEM_MAKE_DIRS) $(ROOT_APACHE_CONF)/conf/extra/httpd-vhosts
	$(SYSTEM_MAKE_DIRS) $(ROOT_APACHE_CONF)/conf/extra/httpd-vhosts-ispcp

# here should be apache,because the ispcp_setup hardcoded it
	$(SYSTEM_MAKE_DIRS) $(SYSTEM_CONF)/apache

	cp -R ./parts   $(SYSTEM_CONF)/apache
	cp -R ./backup  $(SYSTEM_CONF)/apache
	cp -R ./working $(SYSTEM_CONF)/apache

	cp ./httpd.conf      $(SYSTEM_CONF)/apache
	cp ./00_master.conf  $(SYSTEM_CONF)/apache
	cp ./01_awstats.conf $(SYSTEM_CONF)/apache

	cp ./httpd.conf   $(SYSTEM_CONF)/apache/parts/ispcp_base.tpl

	cp ./fcgid.conf   $(SYSTEM_CONF)/apache/fcgid_ispcp.conf
	cp ./fastcgi.conf $(SYSTEM_CONF)/apache/fastcgi_ispcp.conf

uninstall:

	rm -rf $(SYSTEM_CONF)/apache
