# Maintainer: Tomasz P. <tmszppATgmailDOTcom>
pkgname=elements-theme
pkgver=0.0.2
pkgrel=4
pkgdesc="Elements theme for GTK2, GTK3 and Metacity by NanaBuluku"
arch=(any)
url="http://gnome-look.org/content/show.php/Elements?content=145920"
license=('GPL')
depends=(gtk-engine-murrine gtk-engine-unico)
makedepends=(unzip)
source=(http://www.deviantart.com/download/262239294/elements_by_nanabuluku-d4c4p4u.zip)
md5sums=('5207b2e9c85c463d2bfa37489e9bfbd7')

build() {
  cd "$srcdir"
  sed '17i\	text\[NORMAL\]			= \"#ffffff\"' Elements\(GS-and-Classic\)/gtk-2.0/Apps/xfce-panel.rc > xfce-panel.rc.new
  mv -f xfce-panel.rc.new Elements\(GS-and-Classic\)/gtk-2.0/Apps/xfce-panel.rc
}

package() {
  cd "$pkgdir"
  install -d -m755 usr/share/themes
  cp -r $srcdir/Elements\(GS-and-Classic\) usr/share/themes/Elements
  chmod -R a+r usr/share/themes/Elements
}