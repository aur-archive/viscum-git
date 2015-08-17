# Maintainer: ushi <ushi@honkgong.info>
pkgname=viscum-git
pkgver='42.09d71fa'
pkgrel=1
pkgdesc='viscum RSS/ATOM fetching and processing server'
arch=('x86_64')
url='https://github.com/ushis/viscum'
license=('MIT')
depends=('postgresql')
makedepends=('git' 'go' 'godag-hg')
backup=('etc/viscum/viscum.conf' 'etc/viscum/viscumd.conf')
install='viscum.install'
provides=('viscum')
conflicts=('viscum')
source=('viscum::git+https://github.com/ushis/viscum.git#branch=master')
sha256sums=('SKIP')

pkgver() {
  cd viscum
  echo "$(git rev-list --count master).$(git rev-parse --short master)"
}

build() {
  cd viscum
  make
}

package() {
  cd viscum
  make DESTDIR="${pkgdir}/" install
}

# vim:set ts=2 sw=2 et:
