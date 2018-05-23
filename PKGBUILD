# Maintainer: pancho horrillo <pancho at pancho dot name>

_pkgname='ansible-aur'
pkgname="${_pkgname}-git"
pkgver=master.r0.g39541ac
pkgrel=1
pkgdesc='ansible module to install packages from AUR'
arch=('any')
url='https://github.com/kewlfft/ansible-aur'
license=('GPL3')
provides=("${_pkgname}")
conflicts=("${_pkgname}")
source=("git+https://github.com/kewlfft/${_pkgname}.git")
sha512sums=('SKIP')

pkgver() {
    cd "${_pkgname}"
    git describe --all --long | sed 's,^heads/,,;s/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
    cd "${_pkgname}"
    install -Dm644 README.md "$pkgdir/usr/share/doc/${_pkgname}"/README.md
    install -Dm644 aur.py "$pkgdir/usr/share/ansible/plugins/modules/aur.py"
}