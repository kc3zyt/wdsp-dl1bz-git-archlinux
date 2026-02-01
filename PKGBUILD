#Forked from version maintained by Joshua Rubin

pkgname=wdsp-dl1bz-git
_pkgname=wdsp
pkgver=r144.9b308a5
pkgrel=1
pkgdesc='NR0V DSP library ported to linux'
arch=('x86_64')
url='https://github.com/dl1bz/wdsp'
license=('GPL2')
depends=()
makedepends=('git')
provides=("${_pkgname}")
conflicts=("${_pkgname}")
source=("git+$url.git")
md5sums=('SKIP')
sha1sums=('SKIP')
sha256sums=('SKIP')
sha384sums=('SKIP')
sha512sums=('SKIP')

pkgver() {
  cd "$_pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "$_pkgname"
  make NEW_NR_ALGORITHMS=1
}

package() {
  cd "$_pkgname"
  install -D wdsp.h -m 0644 "${pkgdir}/usr/include/wdsp.h"
  install -D libwdsp.so "${pkgdir}/usr/lib/libwdsp.so"
}
