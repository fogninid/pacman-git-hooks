# Maintainer: Daniele Fognini <dfogni@gmail.com>

pkgname=pacman-hooks-git
pkgver=0.1
pkgrel=1
pkgdesc="pacman hooks to autocommit configuration changes during updates to git"
arch=(any)
url="https://code.fognini-depablo.eu/pacman/"
license=('GPL')
depends=(git)
source=(
  "git-check"
  "git-commit"
  "10-git-check.hook"
  "90-git-commit.hook"
)
sha256sums=('8408c1d47d03dd5bb674d8c3cf12a33112e30a3c85e100339736d8b8fc3607d5'
            '88c44626737307d07134f10d1ac1ec3f0568159e78bf369755a13b5c82fa5156'
            '0321ad4803684399849b6cc69b532e47bde22768a34edbc618928a599313b1ca'
            '43033245af1d76df8a0f7c00eb37ed960e9f7cdd3f11da062cc98b550918d130')

package() {
	cd "$srcdir/$_gitname"
	mkdir -p "$pkgdir"/usr/share/libalpm/hooks/bin/
	install 10-git-check.hook "$pkgdir"/usr/share/libalpm/hooks/
	install 90-git-commit.hook "$pkgdir"/usr/share/libalpm/hooks/
	install git-check "$pkgdir"/usr/share/libalpm/hooks/bin/
	install git-commit "$pkgdir"/usr/share/libalpm/hooks/bin/
}
