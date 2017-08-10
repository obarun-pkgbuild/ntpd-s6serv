# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=ntpd-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="ntpd service for s6"
arch=(x86_64)
license=('beerware')
depends=('openntpd' 's6' 's6-rc' 's6-boot')
conflicts=()
install=ntpd-s6serv.install
source=('ntpd.daemon.run.s6'
		'ntpd.log.run.s6'
		'LICENSE')
md5sums=('ab7b5c5a36365129092f81b8a1f17b93'
         '7edbf64064fb9cb05bd226992c6bb4b1'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/ntpd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/ntpd/run"
	
	# log
	install -Dm 0755 "$srcdir/ntpd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/ntpd/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/ntpd-s6serv/LICENSE"
}
