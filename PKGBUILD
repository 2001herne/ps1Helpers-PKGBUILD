# Maintainer: Benjamin Herne <2001herne@gmail.com>

pkgname=ps1Helpers
pkgver=0.1.0
pkgrel=1
pkgdesc=""
arch=('any')
url="https://github.com/2001herne/ps1Helpers"
license=('APACHE')
groups=()
depends=('libgit2')
makedepends=('git'
             'cmake')
provides=("${pkgname%}")
conflicts=("${pkgname%}")
replaces=()
backup=()
options=()
install=
source=("ps1Helpers-$pkgver.tar.gz::https://github.com/2001herne/ps1Helpers/archive/$pkgver.tar.gz")
noextract=()
md5sums=('fc1e1154ae96dacb79590a44a27662e2')

build() {
	cd "$srcdir/${pkgname%}-$pkgver"
    cmake -D CMAKE_BUILD_TYPE=Release .
    make
}

package() {
	cd "$srcdir/${pkgname%}-$pkgver"
    make DESTDIR=${pkgdir} install
}
