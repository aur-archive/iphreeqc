# Maintainer: domanov @ gmail
pkgname=iphreeqc
pkgver=2.18.3
_pkgsvn=5570
pkgrel=3
pkgdesc="IPhreeqc is phreeqc as module for coupling with i.e. Matlab, Python; and Library for Fortran, C, C++."
arch=('i686' 'x86_64')
url="http://wwwbrr.cr.usgs.gov/projects/GWC_coupled/phreeqc/"
license=('custom')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("ftp://brrftp.cr.usgs.gov/pub/charlton/iphreeqc/$pkgname-$pkgver-$_pkgsvn.tar.gz")
md5sums=('a0a93eb17b2095dc235052940b60099e')


build() {
  cd "$srcdir/$pkgname-$pkgver-$_pkgsvn"
  ./configure --prefix=/usr CFLAGS="-mtune=native -O3" CXXFLAGS="-mtune=native -O3"
  make -j4 
}

check() {
  cd "$srcdir/$pkgname-$pkgver-$_pkgsvn"
  make -k check 
}

package() {
  cd "$srcdir/$pkgname-$pkgver-$_pkgsvn"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
