# $Id$
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=dde-device-formatter
pkgver=0.0.1.6
pkgrel=1
pkgdesc='A simple graphical interface for creating file system in a block device'
arch=('x86_64')
url="https://github.com/linuxdeepin/dde-device-formatter"
license=('GPL3')
groups=('deepin-extra')
depends=('qt5-base' 'udisks2-qt5')
makedepends=('deepin-gettext-tools')
source=("$pkgname-$pkgver.tar.gz::https://github.com/linuxdeepin/dde-device-formatter/archive/$pkgver.tar.gz")
sha512sums=('f4934f1f468852cc80c2652169119c0046f306305ceb19e1ee524d6bb159179e98b16ee0d77a85aff73ccf6d03f7fe24d4d6a15d15956a6efb1c8032375451a2')

build() {
  cd dde-device-formatter-$pkgver
  qmake-qt5 PREFIX=/usr
  make
}

package() {
  cd dde-device-formatter-$pkgver
  make INSTALL_ROOT="$pkgdir" install
}