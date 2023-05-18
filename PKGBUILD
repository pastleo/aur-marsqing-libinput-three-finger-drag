# Maintainer: PastLeo <chgu82837@gmail.com>
pkgname=marsqing-libinput-three-finger-drag
pkgver=0.1
pkgrel=1
pkgdesc="Three-finger-drag support for libinput"
arch=('x86_64')
url="https://github.com/marsqing/libinput-three-finger-drag"
license=()
depends=('libinput' 'xdotool')
makedepends=('rust')
source=('marsqing-libinput-three-finger-drag::git+https://github.com/marsqing/libinput-three-finger-drag.git#branch=master')
sha256sums=('SKIP')

build() {
  cd 'marsqing-libinput-three-finger-drag'

  cargo build --release
}

package() {
	mkdir -p "$pkgdir/usr/bin/"

	install -Dm755 "$srcdir/marsqing-libinput-three-finger-drag/target/release/libinput-three-finger-drag" "$pkgdir/usr/bin/libinput-three-finger-drag"
  # TODO: add libinput-three-finger-drag.service for auto-start
}
