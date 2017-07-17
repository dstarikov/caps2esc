pkgname=caps2esc
pkgver=2.0
pkgrel=2
pkgdesc="caps2esc: transforming the most useless key ever in the most useful one"
arch=('i686' 'x86_64')
license=('GPL3')
url="https://github.com/dstarikov/caps2esc"
depends=('libevdev')
makedepends=('gcc')
source=('https://raw.githubusercontent.com/dstarikov/caps2esc/master/caps2esc.c' 'https://raw.githubusercontent.com/dstarikov/caps2esc/master/caps2esc.service')
md5sums=('SKIP' 'SKIP')

build() {
  gcc caps2esc.c -o caps2esc -I/usr/include/libevdev-1.0 -levdev -ludev
}

package() {
  mkdir -p "${pkgdir}/usr/bin"
  cp caps2esc "${pkgdir}/usr/bin"

  mkdir -p "${pkgdir}/etc/systemd/system"
  cp caps2esc.service "${pkgdir}/etc/systemd/system"
}
