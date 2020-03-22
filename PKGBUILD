# Maintainer: Daniele Fognini <dfogni@gmail.com>

pkgname=pacman-hooks-git
pkgver=0.2
pkgrel=2
pkgdesc="pacman hooks to autocommit configuration changes during updates to git"
arch=(any)
url="https://code.fognini-depablo.eu/pacman/"
license=('GPL')
depends=(git)
source=(
  "git-check"
  "git-commit"
  "10-git-check.hook"
  "99-git-commit.hook"
)
sha256sums=('8408c1d47d03dd5bb674d8c3cf12a33112e30a3c85e100339736d8b8fc3607d5'
            '88c44626737307d07134f10d1ac1ec3f0568159e78bf369755a13b5c82fa5156'
            '29553159a31c790234b88cac0a6d94d9c2f03a322ae1c772e25807321f227fbe'
            'a52f6be51c79dc2d505df0375ba1b92d1654146fbf8a470852f40a0afcfb51ca')

package() {
	cd "$srcdir/$_gitname"
	mkdir -p "$pkgdir"/usr/share/libalpm/hooks/
	mkdir -p "$pkgdir"/usr/share/libalpm/scripts/
	install -Dm644 10-git-check.hook "$pkgdir"/usr/share/libalpm/hooks/
	install -Dm644 99-git-commit.hook "$pkgdir"/usr/share/libalpm/hooks/
	install git-check "$pkgdir"/usr/share/libalpm/scripts/
	install git-commit "$pkgdir"/usr/share/libalpm/scripts/
}
