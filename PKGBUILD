
# Maintainer : Mauro Ziliani <mauro@faresoftware.it>

pkgname=ltrace
pkgver=0.7
pkgrel=1
arch=(x86_64)

source=(git+https://gitlab.com/cespedes/ltrace.git)
sha512sums=(SKIP)

prepare() {
    cd ${srcdir}/${pkgname}
    ./autogen.sh
}

build() {
    cd ${srcdir}/${pkgname}
    ./configure --prefix=/usr --without-libunwind
    make
}

package() {
    cd ${srcdir}/${pkgname}
    make DESTDIR=${pkgdir} install
}
