pkgname=screenshu
pkgver=1.0.1
pkgrel=3
pkgdesc="Your favorite screenshooter!"
arch=(i686 x86_64)
url="http://screenshu.com/"
license=('ScreenSHU')
groups=()
depends=(qt)
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(http://screenshu.com/p/_download/latest/lin/screenSHU.tar.gz
        http://screenshu.com/static/media/icon.png
        'screenshu.desktop')
noextract=()
md5sums=('c1b3055b941769041fe11751048739dd'
         'ccb6b738b2d18fd76cdd9b828617e584'
         '416eadf0a6c22d47318253bd81a75a29')

build() {
  cd ${srcdir}
}

package() {
  cd ${srcdir}
  install -d ${pkgdir}/{usr/bin/,opt/}

  # Launcher
  install -D -m644 $srcdir/screenshu.desktop \
  ${pkgdir}/usr/share/applications/screenshu.desktop

  # Icon
  install -D -m644 $srcdir/icon.png \
  ${pkgdir}/usr/share/icons/hicolor/256x256/apps/screenshu.png

  # Program
  install -D -m755 $srcdir/screenSHU \
  ${pkgdir}/usr/bin/
  
  update-desktop-database
}
