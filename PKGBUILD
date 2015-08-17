# Maintainer: TDY <tdy@archlinux.info>

pkgname=pyshaper
pkgver=0.1.3
pkgrel=2
pkgdesc="A simple yet versatile program for managing internet traffic in real time"
arch=('any')
url="http://freenet.mcnabhosting.com/python/pyshaper/"
license=('GPL')
depends=('iproute2' 'python-ezsqlobject' 'python2-pmw' 'tcpdump')
optdepends=('python2-geoip: for filtering remote peers by country')
source=(http://freenet.mcnabhosting.com/python/$pkgname/$pkgname-$pkgver.tar.gz)
sha256sums=('841c9389bdec00717c0da075c370e625ac71683abc03ccf43d582af2bf962e72')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  sed -i '8,11 d' setup.py
  python2 setup.py build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python2 setup.py install --prefix=/usr --root="$pkgdir/"
}

# vim:set ts=2 sw=2 et:
