# Maintainer: Benjamin Herne <2001herne@gmail.com>

pkgname=ps1Helpers-git
pkgver=r2.093513b
pkgrel=1
pkgdesc=""
arch=('any')
url=""
license=('GPL')
groups=()
depends=()
makedepends=('git') # 'bzr', 'git', 'mercurial' or 'subversion'
provides=("${pkgname%-git}")
conflicts=("${pkgname%-git}")
replaces=()
backup=()
options=()
install=
source=('git+ssh://git@github.com/2001herne/ps1Helpers.git')
noextract=()
md5sums=('SKIP')

# Please refer to the 'USING VCS SOURCES' section of the PKGBUILD man page for
# a description of each element in the source array.

pkgver() {
	cd "$srcdir/${pkgname%-git}"

# Git, no tags available
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd "$srcdir/${pkgname%-git}"
    cmake -D CMAKE_BUILD_TYPE=Release .
    make
}

package() {
	cd "$srcdir/${pkgname%-git}"
    make DESTDIR=${pkgdir} install
}
