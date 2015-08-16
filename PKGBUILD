# Maintainer: Rolinh <robinDOThahlingATgw-computingDOTnet>
pkgname=kolekto
pkgver=1.3
pkgrel=2
pkgdesc='A really KISS movie catalog software'
arch=('any')
url='http://pypi.python.org/pypi/kolekto'
license=('MIT')
depends=('kaa-base' 'kaa-metadata' 'python2' 'python2-confiture' 'python2-progressbar' 'python2-requests' 'python2-lxml')
source=(http://pypi.python.org/packages/source/k/${pkgname}/${pkgname}-${pkgver}.tar.gz)
md5sums=('7c3060db2897f9c8370497ec5a477375')

package() {
  cd ${pkgname}-${pkgver}

  sed -i -e 's,^#!/usr/bin/env python$,#!/usr/bin/env python2,' bin/kolekto
  python2 setup.py install --root=${pkgdir} --optimize=1

  install -Dm644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/COPYING"
}

# vim:set ts=2 sw=2 et:
