# Contributor:
# Maintainer:
pkgname=razergenie
pkgver=0.3
pkgrel=0
pkgdesc="Standalone Qt application for configuring Razer devices under GNU/Linux"
url="https://github.com/z3ntu/RazerGenie"
arch="all"
license="GPL3"
depends=""
makedepends="cmake extra-cmake-modules qt5-qtbase-dev"
install=""
#subpackages="$pkgname-dev $pkgname-doc"
source="${pkgname}-${pkgver}.tar.gz::https://github.com/z3ntu/RazerGenie/archive/v$pkgver.tar.gz"
builddir="$srcdir/RazerGenie-$pkgver"

build() {
	cd "$builddir"
	mkdir build && cd build
	cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DKDE_INSTALL_LIBDIR=lib
	make
}

package() {
	cd "$builddir/build"
	make DESTDIR="$pkgdir" install
}

sha512sums="46cd1d8365e4aa90f057fa34e319fcb115ea96255cc42be1fc48e047f63e780ec8ecce3689b6855d41583900139179474240e978fe3af0ceb706f02df15ba39d  razergenie-0.3.tar.gz"
