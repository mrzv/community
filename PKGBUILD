
pkgname=gnupg
pkgver=1.4.15
pkgrel=1
pkgdesc="The OpenPGP part of the GNU Privacy Guard (GnuPG)"
arch=(i386 x86_64)
license=(GPL3)
depends=(bzip2 curl libedit zlib)
source=(ftp://ftp.gnupg.org/gcrypt/gnupg/gnupg-$pkgver.tar.bz2)
url='http://www.gnupg.org/'
md5sums=(58bb873ecf17d3205a98c545248d7b04)

build() {
    cd $srcdir/$pkgname-$pkgver
    ./configure --prefix=/Library/ArchMac \
                --mandir=/Library/ArchMac/man \
                --infodir=/Library/ArchMac/info
    make
}

check() {
    cd $srcdir/$pkgname-$pkgver
    make check
}

package() {
    cd $srcdir/$pkgname-$pkgver
    make DESTDIR=$pkgdir install
}

