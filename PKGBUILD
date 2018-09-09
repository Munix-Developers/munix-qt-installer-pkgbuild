# Maintainer: Mateus Mercer <mateusmercer@gmail.com>
pkgname=munix-installer
pkgver=1.0
pkgrel=4
pkgdesc="Munix distribution installer."
arch=("any")
depends=("qt5-base")
makedepends=("git")
source=("git+https://MatMercer@bitbucket.org/munixdevelopers/${pkgname}.git")
md5sums=("SKIP")

build() {
    cd "${srcdir}/${pkgname}"
    qmake munix-installer.pro
    make
}

package() {
    cd "${srcdir}/${pkgname}"
    install -Dm755 "${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}

