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

	$(SYSTEM_MAKE_DIRS) $(ROOT_CONF)/rc.d

	cp ispcp_daemon  $(ROOT_CONF)/rc.d
	cp ispcp_network $(ROOT_CONF)/rc.d

	chown root:root  $(ROOT_CONF)/rc.d/ispcp_network $(ROOT_CONF)/rc.d/ispcp_daemon
	chmod 0755       $(ROOT_CONF)/rc.d/ispcp_network $(ROOT_CONF)/rc.d/ispcp_daemon

uninstall:

	rm -f $(ROOT_CONF)/rc.d/ispcp_daemon
	rm -f $(ROOT_CONF)/rc.d/ispcp_network
