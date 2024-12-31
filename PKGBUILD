# Maintainer: Stefan Zipproth <s.zipproth@ditana.org>

pkgname=xfce-wallpaper-overlay
pkgver=1.29
pkgrel=1
pkgdesc='Automatically overlays XFCE wallpaper with text from files in ~/.config/xfce-wallpaper-overlay'
arch=('any')
license=('AGPL-3.0-or-later AND MIT-Modern-Variant AND custom:imagemagick AND GPL-2.0-only AND GPL-2.0-or-later AND MIT')
url='https://ditana.org'
depends=('fontconfig' 'imagemagick' 'inotify-tools' 'xfconf' 'xmlstarlet')
source=(
  "file://${PWD}/overlay-wallpaper"
  "file://${PWD}/xfce-wallpaper-overlay.desktop"
  "file://${PWD}/xfce-wallpaper-overlay.1"
)
sha256sums=(
    'SKIP'
    'SKIP'
    'SKIP'
)

package() {
    mkdir -p "$pkgdir/etc/skel/.config/xfce4/wallpaper-overlay"
    install -D -m755 "$srcdir/overlay-wallpaper" "$pkgdir/usr/lib/xfce4/wallpaper-overlay/overlay-wallpaper"
    install -D -m644 "$srcdir/xfce-wallpaper-overlay.desktop" "$pkgdir/etc/xdg/autostart/xfce-wallpaper-overlay.desktop"
    install -D -m644 "$srcdir/xfce-wallpaper-overlay.1" "$pkgdir/usr/share/man/man1/xfce-wallpaper-overlay.1"
}
