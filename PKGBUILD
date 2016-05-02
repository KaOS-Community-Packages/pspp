pkgname=pspp
pkgver=0.10.1
pkgrel=1
pkgdesc="A program for statistical analysis of sampled data."
arch=('x86_64')
url="http://savannah.gnu.org/projects/pspp"
category=Science
screenshot=http://i.imgur.com/2J8lFlY.png
license=('GPL3')
source=("http://mirrors.kernel.org/ubuntu/pool/universe/p/pspp/pspp_${pkgver}-2_amd64.deb")
depends=('ncurses' 'libxml2' 'gsl' 'gtksourceview3' 'libpqxx' )
md5sums=('d89b76eb25869e18f6d83a2545c8247d')
package() {
    tar -xJf data.tar.xz -C $pkgdir
    ln -s /usr/lib/libncursesw.so.6 -T "$pkgdir"/usr/lib/libtinfo.so.5
    ln -s /usr/lib/libtinfo.so.5 -T "$pkgdir"/usr/lib/libtinfo.so
    install -dm755 $pkgdir/usr/share/pixmaps
    cp -a $pkgdir/usr/share/icons/hicolor/scalable/apps/pspp.svg $pkgdir/usr/share/pixmaps/psppire.svg
    rm -r "$pkgdir"{/etc,/usr/share/lintian,/usr/share/info}
    sed -i "s|GTK;Education;Science;Math;|Science;|" $pkgdir/usr/share/applications/pspp.desktop
    }
