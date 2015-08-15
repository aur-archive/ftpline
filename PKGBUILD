# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=FTPLine
pkgname=ftpline
pkgver=1.2.0
pkgrel=2
pkgdesc="A command-line FTP client."
url="http://hackage.haskell.org/package/${_hkgname}"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-ansi-terminal' 'haskell-bytestring=0.9.1.7' 'haskell-directory=1.0.1.1' 'haskell-ftphs' 'haskell-haskeline<0.7' 'haskell-mtl' 'haskell-network=2.2.1.7' 'haskell-strict')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
    install -D -m644 license ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
    rm -f ${pkgdir}/usr/share/doc/${pkgname}/LICENSE
}
md5sums=('12d21595c3c4ae4dc3c774d4adf4a8aa')
