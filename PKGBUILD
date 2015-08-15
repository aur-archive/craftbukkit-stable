# Maintainer: Vincent Post <vincent.post@w1r3.net>
# GitHub: https://github.com/w1r3/archlinux-packages
# Precompiled Packages: http://repo.w1r3.org

pkgname=craftbukkit-stable
pkgver=1.6.4r2.0
pkgrel=2
pkgdesc="Minecraft server implementing the Bukkit API (stable)"
arch=(any)
url="http://bukkit.org"
license=("LGPL")
depends=(java-runtime tmux sudo)
conflicts=(bukkit craftbukkit-git craftbukkit-snapshot)
provides=(bukkit "craftbukkit=1.6.4r2.0")
install=craftbukkit.install
source=("http://dl.bukkit.org/downloads/craftbukkit/get/02389_1.6.4-R2.0/craftbukkit.jar"
"craftbukkit.service"
"craftbukkit.sh")
noextract=("craftbukkit.jar")
md5sums=('5c3d125265a806e842fe97625658fb1c'
         '0ba6b038ca1b04ef1e4f2746e3011a71'
         '0f8a1f5f49ac3b9f9291033ba7f9ed76')

package() {
  install -Dm644 "$srcdir/craftbukkit.jar" "$pkgdir/srv/craftbukkit/craftbukkit.jar"
  install -m755 "$srcdir/craftbukkit.sh" "$pkgdir/srv/craftbukkit/craftbukkit.sh"
  install -Dm644 "$srcdir/craftbukkit.service" "$pkgdir/usr/lib/systemd/system/craftbukkit.service"
}

# vim:set ts=2 sw=2 et:
