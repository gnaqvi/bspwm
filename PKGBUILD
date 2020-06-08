pkgname=bspwm
pkgver=0.9.9
pkgrel=1
pkgdesc='Tiling window manager based on binary space partitioning'
arch=(x86_64)
url='https://github.com/gnaqvi/bspwm'
license=(BSD)
makedepends=(git)
depends=(xcb-util xcb-util-wm xcb-util-keysyms)
optdepends=('sxhkd: to define keyboard and pointer bindings'
            'xdo: for the example panel')
source=("git+$url#branch=rounded_corners")
md5sums=('SKIP')

build() {
  make -C "$pkgname" PREFIX=/usr
}

package() {
  cd "$pkgname"

  make PREFIX=/usr DESTDIR="$pkgdir" install

  # BSD 2-clause
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# getver: -u 2 raw.githubusercontent.com/baskerville/bspwm/master/doc/bspwm.1
# vim: ts=2 sw=2 et:
