# Maintainer: Felipe Magno de Almeida <felipe.m.almeida__at__gmail.com>

pkgbase=gbs
pkgname=python2-gbs
pkgver=20160615
pkgrel=1
pkgdesc="Tizen's gbs project"
arch=('i686' 'x86_64')
license=('GPL')
makedepends=('python2')
source=('git://git.tizen.org/tools/gbs.git'
        'python2.patch')
sha256sums=('SKIP' '56da015d923afa565ba4d141235e4a49964fc92a5c59ae92930de1ccfefc3816')

build() {
  true
}

package() {
  cd $srcdir/gbs
  python2 setup.py install --prefix=/usr --root=$pkgdir
#  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
