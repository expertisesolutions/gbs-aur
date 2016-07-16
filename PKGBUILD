# Maintainer: Felipe Magno de Almeida <felipe.m.almeida__at__gmail.com>

pkgbase=gbs
pkgname=gbs
pkgver=20160615
pkgrel=1
pkgdesc="Tizen's gbs project"
arch=('i686' 'x86_64')
license=('GPL')
depends=('python2' 'python2-git-buildpackage=20160615' 'depanneur=20160615')
optdepends=('python2-librpm-tizen')
source=('git+https://git.tizen.org/cgit/tools/gbs.git#branch=release-20160615'
        'python2.patch')
sha256sums=('SKIP' '56da015d923afa565ba4d141235e4a49964fc92a5c59ae92930de1ccfefc3816')

build() {
  cd $srcdir/gbs
  patch -p1 -i $srcdir/python2.patch
}

package() {
  cd $srcdir/gbs
  python2 setup.py install --prefix=/usr --root=$pkgdir
#  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
