# Maintainer: Tom Brown <tom@CarlsonSpeed.com>
# Contributor: ChatGPT (OpenAI) <https://openai.com> — assisted with Git configuration, and packaging guidance.

pkgname='kdev-templatetools'
pkgver=0.1.0
pkgrel=1
pkgdesc="KDevelop app and file utilities for building and installing your own templates."
arch=('any')
url="https://github.com/TomB16/kdev-templatetools"
license=('MIT')
depends=()  # Add any runtime deps here
makedepends=()
source=("git+https://github.com/TomB16/kdev-templatetools.git#branch=main")  # Fetch from GitHub repo
sha256sums=('SKIP')  # Don't need this when using Git as source


#pkgver() {
#  cd "$srcdir/$pkgname"
#  git describe --tags --always | sed 's/^v//;s/-/./g'
#}


package() {
  cd "$srcdir" || return 1

  # Install scripts
  install -Dm755 "$srcdir/kdev-templatetools/KDevAppTemplateInstall"            "$pkgdir/usr/bin/KDevAppTemplateInstall"
  install -Dm755 "$srcdir/kdev-templatetools/KDevFileTemplateInstall"           "$pkgdir/usr/bin/KDevFileTemplateInstall"

  # Install .desktop file
  install -Dm644 "$srcdir/kdev-templatetools/kdevelop-template.desktop"         "$pkgdir/usr/share/kio/servicemenus/kdevelop-template.desktop"

  # License
  install -Dm644 "$srcdir/kdev-templatetools/LICENSE"                           "$pkgdir/usr/share/licenses/$pkgname/LICENSE"

  # Rebuild KDE service cache
  if command -v kbuildsycoca5 &> /dev/null; then kbuildsycoca5; fi
  if command -v kbuildsycoca6 &> /dev/null; then kbuildsycoca6; fi

}
