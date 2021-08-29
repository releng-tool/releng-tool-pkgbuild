# Maintainer: James Knight <james.d.knight@live.com>

pkgname=releng-tool
pkgver=0.1
pkgrel=1
pkgdesc='tool to assist in the release engineering of a project'
url='https://releng.io/'
arch=('any')
license=('BSD')
makedepends=(
    'python'
)
source=("$pkgname-$pkgver::git+https://github.com/releng-tool/releng-tool.git#tag=v$pkgver")
sha512sums=('SKIP')

build() {
  cd "$pkgname-$pkgver"
  python setup.py build
}

check() {
  cd "$pkgname-$pkgver"
  python setup.py test
}

package() {
  depends=('python')
  cd "$pkgname-$pkgver"
  python setup.py install --root="$pkgdir" --optimize=1

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -dm 755 "$pkgdir/usr/share/bash-completion/completions"
  install -m644 scripts/releng-tool-completion "$pkgdir/usr/share/bash-completion/completions/releng-tool"
}
