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
source=("gcc-h8300-hms.deb::http://ftp.jp.debian.org/debian/pool/main/g/gcc-h8300-hms/gcc-h8300-hms_3.4.6+dfsg2-4_amd64.deb")
md5sums=("f48cc0ee64b75fb4f0adbb98e9db23a3")

package() {
	bsdtar -xf data.tar.xz -C "$pkgdir/"
}
