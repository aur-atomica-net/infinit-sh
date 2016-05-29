# Maintainer: Jason R. McNeil <jason@jasonrm.net>

pkgname=infinit-sh
pkgver=0.5.5
pkgrel=1
pkgdesc="Decentralized Software‑Based File Storage Platform"
arch=('x86_64')
url="https://infinit.sh"
license=('custom')
backup=('etc/conf.d/infinit-sh')
options=(!strip)
source_x86_64=("infinit.tbz::https://storage.googleapis.com/sh_infinit_releases/linux64/infinit-x86_64-linux_debian_oldstable-gcc4-${pkgver}.tbz")
md5sums_x86_64=('fd03427d2814b9985c3cce89653b0ce5')

package() {
    mkdir -p -m755 ${pkgdir}/opt/${pkgname}

    cp -r ${srcdir}/{bin,lib,share} ${pkgdir}/opt/${pkgname}

    mkdir -p -m755 ${pkgdir}/usr/bin
    cd ${pkgdir}/opt/${pkgname}/bin
    for BINARY in *; do
        ln -s /opt/${pkgname}/bin/${BINARY} ${pkgdir}/usr/bin/${BINARY}
    done
}
