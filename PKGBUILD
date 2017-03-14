pkgname=jasper-issue-reader
pkgver=0.2.5
pkgrel=1
pkgdesc="A flexible and powerful issue reader for GitHub"
arch=('i686' 'x86_64')
url="https://jasperapp.io/"
license=() # TODO
depends=()
source=(
https://github.com/jasperapp/jasper/releases/download/v${pkgver}/jasper_v${pkgver}_linux.zip
)

package() {
  mkdir "$pkgdir/opt"
  cp -r "$srcdir/Jasper" "$pkgdir/opt"

  mkdir -p "$pkgdir/usr/bin"
  cat <<'EOF' > "$pkgdir/usr/bin/Jasper"
#!/bin/sh
/opt/Jasper/Jasper $@
EOF
  chmod a+x "$pkgdir/usr/bin/Jasper"
}
md5sums=('cd599760dd7ec9ce495e1dd7400f4e83')
