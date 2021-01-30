# vim:set ts=8 sw=8 et:
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Ralf Zerres <ralf.zerres@networkx.de>

pkgbase=opensips
pkgname=('opensips' 'opensips-modules'
	 'opensips-module-b2bua' 'opensips-module-cpl' 'opensips-module-presence'
	 'opensips-module-berkeley' 'opensips-module-http' 'opensips-module-mysql'
	 'opensips-module-perlvdb' 'opensips-module-postgresql'
	 'opensips-module-sqlite' 'opensips-module-unixodbc' 'opensips-module-text'
	 'opensips-module-virtual' 'opensips-module-cachedb'
	 'opensips-documentation')

pkgver=3.1.1
pkgrel=1
pkgdesc="An Open Source SIP Server able to act as a SIP proxy, registrar, location server, redirect server ..."
url="https://www.opensips.org"
depends=('attr' 'db' 'gcc-libs' 'libxml2' 'openssl')
makedepends=(
	'bison'
	'confuse'
	'doxygen' 'docbook-sgml' 'docbook-utils' 'docbook-xml'
	'expat'
	'flex'
	'hiredis'
	'geoip'
	'json-c'
	'freeradius'
	'libldap>=2.4.18' 'libmariadbclient' 'libmemcached' 'libmicrohttpd'
	'librabbitmq-c' 'libtap-git' 'libutf8proc' 'libuv' 'libxslt'
	'lksctp-tools'
	'lua>=5.1'
	'lynx'
	'mongo-c-driver'
	'net-snmp'
	'osptoolkit'
	'postgresql-libs>=8.4.1'
	'radcli'
	'thrift' 'unixodbc' 'xmlrpc-c' 'zlib'
	)
checkdepends=('expat' 'libtap-git')
arch=('x86_64' 'armv7')
license=('GPL')
options=('!emptydirs' 'zipman' '!makeflags' 'docs')
source=("${pkgbase%%-*}-${pkgver}::https://github.com/OpenSIPS/opensips/archive/${pkgver}.tar.gz"
	usr_lib_systemd_system_opensips.service
	usr_lib_tmpfiles.d_opensips.conf)
sha256sums=('a4bc1f144af12e6e0984c5886a54b96ef203ea2a4b58df3701f8eadc795d083a'
	    'c2fec4be085b108db10834fa9832e98d696c2de6408f85f96cf89c13bf6be819'
	    'ee2baa9bc7b7fb1612b3eeffb9f8d23abdde20b2154d0756f3351344e4e75b7d')
changelog="$pkgname.changelog"
validpgpkeys=( # Ralf Zerres (Package Signing)
	       '1EC4BE4FF2A6C9F4DDDF30F33C5F485DBD250D66'
	     )

# Database modules
modules_http=('modules/db_http')
modules_oracle=('modules/db_oracle')
modules_mysql=('modules/db_mysql')
modules_perlvdb=('modules/db_perlvdb')
modules_postgresql=('modules/db_postgres')
modules_sqlite=('modules/db_sqlite')
modules_text=('modules/db_text')
modules_unixodbc=('modules/db_unixodbc')
modules_virtual=('modules/db_virtual')

modules_cachedb=('cachedb_cassandra'
		 #'cachedb_couchbase'
		 'cachedb_local' 'cachedb_memcached'
		 'cachedb_mongodb' 'cachedb_redis' 'cachedb_sql')

# Commandline parser modules
modules_cpl=('cpl_c')

# Application specific modules
modules_b2bua=('b2b_entities' 'b2b_logic' 'b2b_sca')
modules_presence=('presence' 'presence_callinfo' 'presence_dfks'
		  'presence_dialoginfo' 'presence_mwi'
		  'presence_xcapdiff' 'presence_xml'
		  'pua' 'pua_bla' 'pua_dialoginfo' 'pua_mi'
		  'pua_usrloc' 'pua_xmpp')

# General purpose modules
modules_base=('aaa_radius'
	      'acc'
	      'alias_db'
	      'auth' 'auth_aaa' 'auth_db' 'auth_jwt'
	      'avpops'
	      'benchmark'
	      'call_center' 'call_control' 'callops'
	      'carrierroute'
	      'cfgutils'
	      'cgrates'
	      'cluster'
	      'compression'
	      'dialog'
	      'dialplan'
	      'dispatcher'
	      'diversion'
	      'dns_cache'
	      'domain'
	      'domainpolicy'
	      'drouting'
	      'emergency'
	      'enum'
	      'event_datagram' 'event_flatstore' 'event_rabbitmq' 'event_route'
	      'event_routing' 'event_stream' 'event_virtual' 'event_xmlrpc'
	      'exec'
	      'fraud_detection'
	      'freeswitch' 'freeswitch_scripting'
	      'gflags'
	      'group'
	      'h350'
	      'identity'
	      'imc'
	      'jabber'
	      'json' 'jsonrpc'
	      'ldap'
	      'load_balancer'
	      'lua'
	      'mangler'
	      'mahops'
	      'maxfwd'
	      'media_exchange'
	      'mediaproxy'
	      'mid_registrar'
	      'mi_datagram' 'mi_fifo' 'mi_html' 'mi_http' ' mi_xmlrpc_ng'
	      'mmgeoip'
	      'msilo'
	      'nathelper'
	      'nat_traversal'
	      'options'
	      'path'
	      'peering'
	      'perl'
	      'permissions'
	      'pi_http'
	      'pike'
	      'proto_bin' 'proto_hep' 'proto_sctp' 'proto_smpp' 'proto_tls' 'proto_ws' 'proto_wss'
	      'python'
	      'qos' 'qrouting'
	      'rabbitmq' 'rabbitmq_consumer'
	      'rate_cacher' 'ratelimit'
	      'regex'
	      'registrar'
	      'rest_client'
	      'rls'
	      'rr'
	      'rtpengine' 'rtpproxy'
	      'script_helper'
	      'signaling'
	      'sipcapture'
	      'sip_i' 'sipmsgops' 'siprec'
	      'sl'
	      #'sngtc'
	      'snmpstats'
	      'speeddial'
	      'sql_cacher'
	      'sst'
	      'statistics'
	      'stir_shaken'
	      'stun'
	      'textops'
	      'tls_mgm'
	      'tm'
	      'topology_hiding'
	      'tracer'
	      'uac' 'uac_auth' 'uac_redirect' 'uac_registrant'
	      'userblacklist' 'usrloc'
	      'uuid'
	      'xcap' 'xcap_client'
	      'xml'
	      'xmpp')

prepare() {
	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	if [ -h "$srcdir"/Makefile.conf.template ]; then
		msg2 "preset Makefile.conf template"
		test ! -f Makefile.conf.template.orig  &&
		mv Makefile.conf.template Makefile.conf.template.orig
		cp "$srcdir"/Makefile.conf.template Makefile.conf.template
	fi

	# since 3.0 use upstream file
	#cp "$srcdir"/Makefile.defs Makefile.defs

	if [ ! -f .makepkg-patched ]; then
		if [ ! -d ./.git ]; then
			msg2 "patching: create orphan git repository"
			git init -b opensips-${pkgver}
			git checkout --orphan ${pkgbase%%-*}-${pkgver}
			msg2 "patching: create commits corresponding to version ${pkgver}"
			git add -A
			git commit -m "opensips ${pkgver}"

		fi
		cp ../../rabbitmq_consumer.xml modules/rabbitmq_consumer/doc/rabbitmq_consumer.xml
		git add modules/rabbitmq_consumer/doc/rabbitmq_consumer.xml
		git commit -am "rabbitmq_consumer.xml"
		#git add Makefile.defs
		#git commit -am "opensips-${pkgver}: Makefile.defs"
		if [ -d ../../patches-git-${pkgver} ]; then
			git am --signoff ../../patches-git-${pkgver}/0001-packaging-Arch-Linux-update-search-path-for-docbook.patch
		fi
		msg2 " patching [done]"
		touch .makepkg-patched
		#echo "  -> no patches for branch '${_branch}' needed"
	fi

	if [ ! -f "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/INSTALL.archlinux" ]; then
		cp ../../INSTALL.archlinux "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/INSTALL.archlinux"
	fi

	#msg2 "ensure python2 usage (<=v3.0)"
	#for file in $(find . -name '*.py' -print); do
	#	sed -i 's_^#!.*/usr/bin/python_#!/usr/bin/python2_' $file
	#	sed -i 's_^#!.*/usr/bin/env.*python_#!/usr/bin/env python2_' $file
	#done

	msg2 "ensure binaries live in /bin and /usr/bin"
	sed -i 's|sbin|bin|g' Makefile
	sed -i 's|bin-dir = sbin/|bin-dir = bin/|' Makefile.defs
}

build() {
	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	#FASTER=1
	make -j$(nproc) \
		#include_modules="${_modules}" \
		LIBDIR=lib \
		PREFIX=/usr \
		skip_modules="cachedb_couchbase db_oracle sngtc"
}

package_opensips() {
	pkgdesc="A very fast and flexible SIP Server (RFC3261, stable version)"

	depends=(
		'confuse' 'geoip' 'json-c'
		'libtap-git' 'libuv' 'libxslt'
		'lksctp-tools')
	optdepends=(
		'cassandra-cpp-driver: cassandra C++ support'
		'curl: curl support'
		'confuse: confuse support'
		'lksctp-tools: sctp support'
		'lynx: text browser support'
		'hiredis: HiRedis support'
		'libldap: LDAP support'
		'libmariadbclient: Maria DB support'
		'libmaxminddb: MaxMin DB support'
		'libmemcached: Memory caching support'
		'libmicrohttpd: Inline HTTPD support'
		'librabbitmq-c: Rabbitmq C support'
		'libsasl: SASL authentication support'
		'libutf8proc: UTF8 processing support'
		'lua: LUA scripting support'
		'mariadb-libs: Maria-DB support'
		'mongo-c-driver: C-Interface for Mongo-DB support'
		'net-snmp: SNMP support'
		'osptoolkit: OSP Toolkit support'
		'pcre: Perl Regular-Expression support'
		'perl: Perl support'
		'postgresql-libs: PostgreSQL-DB support'
		'python2: Python v2 support'
		'radcli: RAD commandline support'
		'rabbitmq: Rabbit CacheMemory support'
		'thrift: Thrift support'
		'unixodbc: UNIX ODBC support')
	install=opensips.install

	provides=("opensips=${pkgver}")
	conflicts=('opensips-git')

	_components=('opensips')
	backup=(
		"etc/opensips/opensips.cfg"
		"etc/opensips/regex_groups.cfg"
	)

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	# install app only, excluding console, modules and modules docs
	for _cmp in ${_components[@]}; do
		make \
			BASEDIR="$pkgdir" \
			PREFIX=/usr \
			LIBDIR=lib \
			install-app

		# Conforms to the arch packaging standards (https://wiki.archlinux.org/index.php/Arch_Packaging_Standards)
		mkdir -p "$pkgdir"/etc/
		mv "$pkgdir"/usr/etc/opensips/ "$pkgdir"/etc/
		sed -i 's#mpath=".*lib/opensips/modules/"#mpath="/usr/lib/opensips/modules/"#' "$pkgdir"/etc/opensips/opensips.cfg

		# fix bad paths
		cd "$pkgdir"/usr/share
		find -type f -exec sed -i "s#"$pkgdir"##" {} \;

		mv "$pkgdir"/usr/sbin "$pkgdir"/usr/bin

		cd "$pkgdir"/etc
		find -type f -exec sed -i "s#"$pkgdir"##" {} \;

		# python2 is being used
		#cd "$pkgdir"
		#grep -lR '#!.*python' * | while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done

		# Systemd files
		install -Dm0644 "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/${pkgname}.service" "$pkgdir"/usr/lib/systemd/system/${pkgname}.service
		install -Dm0644 "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/${pkgname}.tmpfiles.conf" "$pkgdir"/usr/lib/tmpfiles.d/${pkgname}.conf
		if [ -f "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/INSTALL.archlinux" ]; then
			install -Dm0644 "${srcdir}/${pkgbase%%-*}-${pkgver}/packaging/arch/INSTALL.archlinux" "$pkgdir"/usr/share/doc/${pkgname}/INSTALL.archlinux
		fi
	done
}

# base modules
package_opensips-modules() {
	pkgdesc="A fast and flexible SIP Server - base modules (stable version)"
	depends=('opensips')
	provides=("opensips-modules=${pkgver}")
	conflicts=('opensips-modules-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	# install app only, excluding console, modules and modules docs
	for _module in ${modules_base[@]}; do
		make \
			BASEDIR="$pkgdir" \
			PREFIX=/usr \
			LIBDIR=lib \
			modules=modules/${_module} \
			install-modules
	done
}

# Application specific modules
package_opensips-module-b2bua() {
	pkgdesc="A fast and flexible SIP Server - B2B User-Agent modules (stable version)"
	depends=('opensips')
	provides=("opensips-modules-b2bua=${pkgver}")
	conflicts=('opensips-modules-b2bua-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	for _module in ${modules_b2bua[@]}; do
		make \
			BASEDIR="$pkgdir" \
			PREFIX=/usr \
			LIBDIR=lib \
			modules=modules/${_module} \
			install-modules
	done
}

package_opensips-module-cpl() {
	pkgdesc="A fast and flexible SIP Server - Call Processing Language module (stable version)"
	depends=('opensips')
	provides=("opensips-modules-cpl=${pkgver}")
	conflicts=('opensips-modules-cpl-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules=modules/$modules_cpl \
		install-modules
}

package_opensips-module-presence() {
	pkgdesc="A fast and flexible SIP Server - Presence handling modules (stable version)"
	depends=('opensips')
	provides=("opensips-modules-presence=${pkgver}")
	conflicts=('opensips-modules-presence-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	for _module in ${modules_presence[@]}; do
		make \
			BASEDIR="$pkgdir" \
			PREFIX=/usr \
			LIBDIR=lib \
			modules=modules/${_module} \
			install-modules
	done
}

# Database modules
package_opensips-module-berkeley() {
	pkgdesc="A fast and flexible SIP Server - database module Berkeley (stable version)"
	depends=('opensips')
	provides=("opensips-modules-berkeley=${pkgver}")
	conflicts=('opensips-modules-berkeley-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_berkeley" \
		install-modules
}

package_opensips-module-flatstore() {
	pkgdesc="A fast and flexible SIP Server - database module Flatstore (stable version)"
	depends=('opensips')
	provides=("opensips-modules-flatstore=${pkgver}")
	conflicts=('opensips-modules-flatstore-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_flatstore" \
		install-modules
}

package_opensips-module-http() {
	pkgdesc="A fast and flexible SIP Server - database module HTTP (stable version)"
	depends=('opensips')
	provides=("opensips-modules-http=${pkgver}")
	conflicts=('opensips-modules-http-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_http" \
		install-modules
}

package_opensips-module-mysql() {
	pkgdesc="A fast and flexible SIP Server - database module MySQL (stable version)"
	depends=('opensips' 'mariadb')
	provides=("opensips-modules-mysql=${pkgver}")
	conflicts=('opensips-modules-mysql-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_mysql" \
		install-modules
}

package_opensips-module-oracle() {
	pkgdesc="A fast and flexible SIP Server - database module Oracle (stable version)"
	depends=('opensips' 'oracle')
	provides=("opensips-modules-oracle=${pkgver}")
	conflicts=('opensips-modules-oracle-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_oracle" \
		install-modules
}

package_opensips-module-perlvdb() {
	pkgdesc="A fast and flexible SIP Server - database module Perl virtual DB (stable version)"
	depends=('opensips')
	provides=("opensips-modules-perlvdb=${pkgver}")
	conflicts=('opensips-modules-perlvdb-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_perlvdb" \
		install-modules
}

package_opensips-module-postgresql() {
	pkgdesc="A fast and flexible SIP Server - database module PostgreSQL (stable version)"
	depends=('opensips' 'postgresql')
	provides=("opensips-modules-postgresql=${pkgver}")
	conflicts=('opensips-modules-postgresql-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_postgresql" \
		install-modules
}

package_opensips-module-sqlite() {
	pkgdesc="A fast and flexible SIP Server - database module SQlite (stable version)"
	depends=('opensips' 'sqlite')
	provides=("opensips-modules-sqlite=${pkgver}")
	conflicts=('opensips-modules-sqlite-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_sqlite" \
		install-modules
}

package_opensips-module-unixodbc() {
	pkgdesc="A fast and flexible SIP Server - database module UnixODBC (stable version)"
	depends=('opensips' 'unixodbc')
	provides=("opensips-modules-mysql=${pkgver}")
	conflicts=('opensips-modules-mysql-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_unixodbc" \
		install-modules
}

package_opensips-module-text() {
	pkgdesc="A fast and flexible SIP Server - database module text (stable version)"
	depends=('opensips')
	provides=("opensips-modules-text=${pkgver}")
	conflicts=('opensips-modules-text-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_text" \
		install-modules
}

package_opensips-module-virtual() {
	pkgdesc="A fast and flexible SIP Server - virtual database module  (stable version)"
	depends=('opensips')
	provides=("opensips-modules-virtual=${pkgver}")
	conflicts=('opensips-modules-virtual-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		modules="$modules_virtual" \
		install-modules
}

package_opensips-module-cachedb() {
	pkgdesc="A fast and flexible SIP Server - database modules for caching (stable version)"
	depends=('opensips')
	provides=("opensips-modules-cachedb=${pkgver}")
	conflicts=('opensips-modules-cachedb-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	for _module in ${modules_cachedb[@]}; do
		make \
			BASEDIR="$pkgdir" \
			PREFIX=/usr \
			LIBDIR=lib \
			modules=modules/${_module} \
			install-modules
			#skip_modules="cachedb_couchbase"
	done
}

# Offline documentation
package_opensips-documentation() {
	pkgdesc="A fast and flexible SIP Server - documentation (stable version)"
	suggests=('opensips')
	provides=("opensips-documentation=${pkgver}")
	conflicts=('opensips-documentation-git')

	cd "$srcdir"/${pkgbase%%-*}-${pkgver}

	msg2 "create documentation targets"
	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		doxygen modules-docbook-html
		# modules-docbook-pdf \
		#dbschema-docbook-html dbschema-docbook-pdf \
		#modules-readme

	msg2 "install documentation targets"
	make \
		BASEDIR="$pkgdir" \
		PREFIX=/usr \
		LIBDIR=lib \
		install-doc \
		install-modules-docbook

	msg2 " ... text files"
	DOC_DIR="$pkgdir/usr/share/doc/${pkgbase%%-*}"
	if [ -d "$DOC_DIR/txt" ]; then
		mkdir -p "$DOC_DIR/txt"
		chmod 0755 "$DOC_DIR/txt"
		mv --recursive $DOC_DIR/README.* "$DOC_DIR/txt"
		chmod --recursive 0644 "$DOC_DIR/txt"
	fi

	msg2 " ... html documents"
	DOC_DIR="$pkgdir/usr/share/doc/${pkgbase%%-*}"
	if [ -d "$DOC_DIR/html" ]; then
		mkdir -p "$DOC_DIR/html"
		chmod 0755 "$DOC_DIR/html"
		mv --recursive $DOC_DIR/*.html "$DOC_DIR/html"
		chmod --recursive 0644 "$DOC_DIR/html"
	fi

	msg2 " ... examples"
	DOC_DIR="$pkgdir/usr/share/doc/${pkgbase%%-*}"
	if [ -d ./examples ]; then
		mkdir -p "$DOC_DIR"
		cp --recursive ./examples "$DOC_DIR"
		chmod --recursive 0644 "$DOC_DIR"
	fi
}
