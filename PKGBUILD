# Maintainer: Chris Sakalis <chrissakalis@gmail.com>
# Contributor: Fred Romano <f r e d r o m a n o AT g m a i l DOT c o m>
# Contributor: Matz Radloff <m a t z r a d l o f f AT g o o g l e m a i l DOT c o m>
# Contributor: David J. Haines <d h a i n e s AT g m a i l DOT c o m>

pkgname=minutor
pkgver=2.0.1
pkgrel=1
pkgdesc="A minimalistic map generator for minecraft."
arch=('i686' 'x86_64')
url="http://seancode.com/minutor/"
license=('BSD')
depends=(qt5-base)
source=("http://seancode.com/minutor/$pkgver/minutor_$pkgver.tar.gz" "license.txt")
md5sums=('e3681a502af767d8f9edbc595b723ed0'
         'c169d81765c3f73db7353a198ca9fb98')
sha256sums=('ca209d3b15a38894cfabb9420d2b1b20a8843a4992f91a35ab3168bf25b09ec1'
            '7225ca2e326c72e6342d2aa188c3c38156d9a827276b46d6a8736c68819a34f6')

build()
{
	cd "$srcdir/$pkgname-$pkgver"
	qmake
	make
}

package()
{
	cd "$srcdir/$pkgname-$pkgver"
	make INSTALL_ROOT="$pkgdir/" install
	cd "$srcdir"
	install -Dm644 license.txt "$pkgdir/usr/share/licenses/$pkgname/license.txt"
}
