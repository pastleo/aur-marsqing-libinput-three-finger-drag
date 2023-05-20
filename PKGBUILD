# Maintainer: PastLeo <chgu82837@gmail.com>
pkgname=marsqing-libinput-three-finger-drag
pkgver=0.1
pkgrel=2
pkgdesc="Three-finger-drag support for libinput"
arch=('x86_64')
url="https://github.com/marsqing/libinput-three-finger-drag"
license=()
depends=('libinput' 'xdotool')
makedepends=('rust')
source=('marsqing-libinput-three-finger-drag::git+https://github.com/marsqing/libinput-three-finger-drag.git#branch=master'
        'libinput-three-finger-drag.service')
sha256sums=('SKIP'
            'af3c4fc31614dd95989ed1dee4bad0379e45b0dfce81a9cdda0b4e1e454eb16b')

build() {
  cd 'marsqing-libinput-three-finger-drag'

  cargo build --release
}

package() {
  mkdir -p "$pkgdir/usr/bin/"

  install -Dm755 "$srcdir/marsqing-libinput-three-finger-drag/target/release/libinput-three-finger-drag" "$pkgdir/usr/bin/libinput-three-finger-drag"
  install -Dm644 "$srcdir/libinput-three-finger-drag.service" "$pkgdir/usr/lib/systemd/user/libinput-three-finger-drag.service"
}
