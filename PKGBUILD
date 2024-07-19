# Author: Torkus
# Maintainer: Torkus <48141663+ogri-la@users.noreply.github.com>
pkgname=strongbox
pkgver=7.4.0
pkgrel=1
pkgdesc="World of Warcraft addon manager. F/OSS, ad-free and privacy respecting."
arch=("x86_64")
url="https://github.com/ogri-la/strongbox"
license=("AGPL")
depends=("zlib" "fuse2")
options=("!strip" "!debug")
provides=("$pkgname")
changelog="changelog"
conflicts=("$pkgname")
replaces=("wowman")
noextract=("$pkgname-$pkgver")

# "strongbox-1.2.3::https://github.com/ogri-la/strongbox/releases/download/1.2.3/strongbox-1.2.3-x86_64.AppImage"
source=(
    "$pkgname-$pkgver::https://github.com/ogri-la/strongbox/releases/download/$pkgver/$pkgname-$pkgver-x86_64.AppImage"
    "$pkgname.desktop"
)

strongbox_sha256="6e2cc13ba812539c6c5ca035c3ec019b8e78d8c4e664a4a1b4e3e8b8ac83df72"
strongbox_desktop_sha256="b021ee257f90c04e05e8819774956fe51a7312f126884d9a71b12e067df48aa4"
sha256sums=(
    "$strongbox_sha256"
    "$strongbox_desktop_sha256"
)

package() {
    install -Dm755 "$pkgname-$pkgver" "$pkgdir/usr/bin/$pkgname"
    install -Dm644 "$pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop"
}
