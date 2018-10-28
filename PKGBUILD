pkgname=zeal
pkgver=0.6.1
pkgrel=1
pkgdesc="A simple offline documentation browser inspired by Dash"
arch=('x86_64')
license=('GPL3')
url="https://zealdocs.org/"
depends=('qt5-base')
makedepends=('qt5-tools' 'cmake')
categories=('development')
source=(https://github.com/zealdocs/${pkgname}/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.xz)
md5sums=('3d20e9b4190bc53616039341440e8a01')

build() {
  mkdir -p build
  cd build

  cmake ../${pkgname}-${pkgver} \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd build

  make DESTDIR=${pkgdir} install
}
