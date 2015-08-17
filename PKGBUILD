# Maintainer: Sergey Malkin <adresatt@gmail.com>
pkgname=tinymount
pkgver=0.2.0
pkgrel=3
pkgdesc="Simple GUI tool for disks mounting written in c++/Qt"
arch=('x86_64' 'i686')
url="https://github.com/limansky/tinymount"
license=('GPL')
depends=('qt4')
source=(https://github.com/downloads/limansky/tinymount/${pkgname}-${pkgver}.tar.bz2)
md5sums=('3356db6359a64a3f4faf8e48ce68da7d')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}/"
  qmake PREFIX=/usr ${pkgname}.pro
  make || return 1
  make INSTALL_ROOT=${pkgdir} install || return 1
}
