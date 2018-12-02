# Maintainer: Erik Dubois <erik.dubois@gmail.com>
pkgname=arcolinux-calamares-gzr-xfce-git
_pkgname=arcolinux-gzr-calamares-xfce
_destname="/etc/calamares"
_licensedir="/usr/share/arcolinux/licenses/"
pkgver=18.11
pkgrel=1
pkgdesc="calamares for arco-gzr"
arch=('any')
url="https://github.com/Arcolinux-GzR/arcolinux-gzr-calamares-xfce"
license=('GPL3')
makedepends=('git')
depends=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${_pkgname}::"git+https://github.com/Arcolinux-GzR/${_pkgname}.git")
sha256sums=('SKIP')
install='readme.install'
package() {
	rm -f "${srcdir}/${_pkgname}/"README.md
	rm -f "${srcdir}/${_pkgname}/"git-v*
	rm -f "${srcdir}/${_pkgname}/"setup-git-v*
	mkdir -p "${pkgdir}${_licensedir}${_pkgname}"
	mv "${srcdir}/${_pkgname}/"LICENSE "${pkgdir}${_licensedir}${_pkgname}/LICENSE"
	mkdir -p "${pkgdir}${_destname}"
	cp -r "${srcdir}/${_pkgname}/calamares/"* "${pkgdir}${_destname}"
}
