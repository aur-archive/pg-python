# Maintainer: Gianni Vialetto <gianni at rootcube dot net>

pkgname=pg-python
pkgver=1.0.1
pkgrel=1
pkgdesc="Alternative python3 PL implementation for PostgreSQL"
arch=('i686' 'x86_64')
url="http://python.projects.postgresql.org/backend/"
license=('BSD')
depends=('postgresql>=9.1', 'python>=3.1')
install='pg-python.install'
source=("http://python.projects.postgresql.org/backend/files/$pkgname-$pkgver.tar.bz2")
md5sums=('21c00731b59a036b82d9de853905c312')
sha256sums=('d9f1d8bea63f9edaa454bf41eb74a440f3c15f0c750176ee2c1b98290f8e897b')
sha512sums=('85dc2b03bd99d53e20ab0c788d9dd808545c2484bfa5ba155d4c2691a4e0f4bcfba0b964297e9678806564b12fbef40862b7ef9ab34846f0cb1d256d27be2798')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  
  ./configure
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  
  make DESTDIR="$pkgdir" install
}

