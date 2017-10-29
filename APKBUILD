# Contributor:
# Maintainer:
pkgname=razergenie
pkgver=0.4
pkgrel=0
pkgdesc="Standalone Qt application for configuring Razer devices under GNU/Linux"
url="https://github.com/z3ntu/RazerGenie"
arch="all"
license="GPL3"
depends="openrazer-daemon"
makedepends="cmake extra-cmake-modules qt5-qtbase-dev"
install=""
source="https://github.com/z3ntu/RazerGenie/releases/download/v$pkgver/RazerGenie-$pkgver.tar.xz"
builddir="$srcdir/RazerGenie-$pkgver/build"

prepare() {
    mkdir -p "$builddir"
}

build() {
	cd "$builddir"
	cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DKDE_INSTALL_LIBDIR=lib
	make
}

package() {
	cd "$builddir"
	make DESTDIR="$pkgdir" install
}

sha512sums="b8ea90f982ed25231c10c7244615c8e6db97cb36a7740ab02855c0c5efdf22c19f8c770f1d51080f8d5d68ff6c212f290fc213bf393baf60517fe622b8b77cc9  RazerGenie-0.4.tar.xz"
