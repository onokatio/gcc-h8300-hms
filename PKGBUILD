# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=gcc-h8300-hms
pkgver=3.4.6
pkgrel=1
pkgdesc="h8300 cross GCC"
arch=('x86_64')
url=""
license=('GPL')
groups=()
depends=('binutils-h8300-hms')
privedes=('gcc-h8300-hms')
makedepends=()
install=
source=("http://ftp.tsukuba.wide.ad.jp/software/gcc/releases/gcc-$pkgver/gcc-$pkgver.tar.gz")
md5sums=("ca4c4f28adbe0a657a3caa5c2bc45156")

build() {
	cd $srcdir
	./configure \
		--target=h8300-hms \
		--with-newlib \
		--enable-languages=c,c++ \
		--disable-libssp \
		--enable-obsolete \
		--prefix=/usr
	make
}
package() {
	bsdtar -xf data.tar.xz -C "$pkgdir/"
}
