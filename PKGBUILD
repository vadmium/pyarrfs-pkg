_proj=pyarrfs
pkgname="$_proj"
pkgver="0.8.1"
pkgrel=1
pkgdesc="File system that represents Rar files as directories"
arch=(any)
license=(MIT)
url="http://labs.spritelink.net/$_proj"
depends=(python2 python-fuse "python2-rarfile>=2.3")
makedepends=(python2 python-fuse "python2-rarfile>=2.3")

#_pypi_source
_rls="$_proj-$pkgver"
source+=(
"https://pypi.python.org/packages/source/${_proj:0:1}/$_proj/$_rls.tar.gz")
md5sums+=(fbe1125b4f85dd8400002db6c8e23551)

package() {
    cd "$srcdir/$_rls"
    python2 setup.py install --root="$pkgdir" --optimize=1
    install -D -m644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
