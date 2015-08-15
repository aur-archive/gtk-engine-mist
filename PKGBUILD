# Maintainer: Edoardo Maria Elidoro <edoardo.elidoro@gmail.com>
# Maintainer: Vinycius Maia <suportevg@uol.com.br>

pkgname=gtk-engine-mist
pkgver=2.91.1
pkgrel=1
pkgdesc="Mist theme engine for GTK+ 2"
arch=(i686 x86_64)
license=('GPL' 'LGPL')
depends=('gtk2>=2.20.0')
makedepends=('pkgconfig' 'intltool')
options=('!libtool')
url="http://live.gnome.org/GnomeArt"
source=(http://ftp.gnome.org/pub/gnome/sources/gtk-engines/2.91/gtk-engines-${pkgver}.tar.bz2)
md5sums=('290d2fdb66743066dab92db694dd7b99')

package() {
  cd "${srcdir}/gtk-engines-${pkgver}"
  ./configure --prefix=/usr --disable-all --enable-mist || return 1
  make || return 1
  make DESTDIR="${pkgdir}" install || return 1
}
