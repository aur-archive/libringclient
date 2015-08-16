pkgname=libringclient
pkgver=0.3.0
pkgrel=1
pkgdesc="Official API of the Ring communication framework"
license=('LGPL')
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/uranie/"
depends=('ring-daemon' 'qt5-base')
makedepends=('cmake')
source=("git+git://anongit.kde.org/libringclient#tag=${pkgver}")
md5sums=('SKIP')

prepare() {
  cd "${srcdir}/libringclient"
}

build() {
  cd "${srcdir}/libringclient"
  cmake -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr .
  make
}

package() {
  cd "${srcdir}/libringclient"
  make DESTDIR="$pkgdir" install
}

