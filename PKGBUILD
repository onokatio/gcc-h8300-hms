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
source=("http://ftp.tsukuba.wide.ad.jp/software/gcc/releases/gcc-$pkgver/gcc-$pkgver.tar.gz"
 "https://sourceware.org/pub/newlib/newlib-1.19.0.tar.gz")
md5sums=(SKIP SKIP)

prepare() {
	mkdir $srcdir/../build
}
build() {
	#cd $srcdir/../build
	#$srcdir/gcc-$pkgver/configure \
	cd $srcdir/gcc-$pkgver
	ln -s $srcdir/newlib-1.19.0/newlib .
	./configure \
		--target=h8300-hms \
		--with-newlib \
		--without-headers \
		--enable-languages=c \
		--disable-libssp \
		--disable-nls \
		--disable-libstdc__-v3 \
		--disable-shared \
		--disable-libada \
		--disable-werror \
		--prefix=/usr
	make all-gcc
}
package() {
	cd $srcdir/build
	make DESTDIR="$pkgdir" install
}
