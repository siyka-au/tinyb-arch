# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=tinyb
pkgver=0.5.1
pkgrel=1
epoch=
pkgdesc="Intel Tiny Bluetooth LE Library"
arch=(x86_64)
url="https://github.com/intel-iot-devkit/tinyb"
license=('MIT')
groups=()
depends=("bluez")
makedepends=("cmake")
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/intel-iot-devkit/$pkgname/archive/v$pkgver.tar.gz")
noextract=()
sha256sums=("1d27b5f3b05c5b7a9f29f3d717164162607aa94b8e15ba2a9aaa3884908a2da1")
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
}

build() {
	cd "$pkgname-$pkgver"
	mkdir -p build
	cd build
	cmake -DCMAKE_INSTALL_PREFIX=$pkgdir/usr/ ..
	make
}
package() {
	cd "$pkgname-$pkgver"
	cd build
	make install
}
