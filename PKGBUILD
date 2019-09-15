# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=tre-init
pkgver=1.28.1
pkgrel=1
pkgdesc="Command line tools for tre"
arch=('any')
url=""
license=('AGPLv3')
groups=()
depends=('nodejs')
makedepends=('npm')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
source=()

pkgver () {
  npm view ${pkgname}@latest version
}

package () {
  source "$HOME/.nvm/nvm.sh"
  nvm use 10.8.0
  local _npmdir="${pkgdir}/usr/lib/node_modules/"
  mkdir -p $_npmdir
  npm install -g --prefix "${pkgdir}/usr" ${pkgname}@${pkgver}
}
