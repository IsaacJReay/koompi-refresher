pkgname=koompi-refresher
pkgver=2.0
pkgrel=1
pkgdesc='Refresher for KOOMPI'
arch=(x86_64)
url="https://koompi.com"
install="$pkgname.install"
license=('custom')
# depends=('plasma')
source=(
    "file://refresher_20201016.tar.gz"
    "$pkgname.install"
)
sha256sums=(
    '54a7f85866722ee024ff40884d9b1d6ac0a103081cea9bb8ff091163c0f1588e'
    '01f9d54c0b893197dd8c2e2f9098a4f03ae77536346337e00597f78f9a5a085b'
)

build(){
    tar -xzvpf "${srcdir}/refresher_20201016.tar.gz" -C "${srcdir}"
}

package() {
    install -Dm755 "${srcdir}/refresher/source/root/usr/bin/refresher" -t "${pkgdir}/usr/bin/"
    install -Dm755 "${srcdir}"/refresher/source/root/usr/share/org.koompi.refresher/{panel-dark.js,panel-light.js,widget.js} -t "${pkgdir}/usr/share/org.koompi.refresher"
    install -Dm755 "${srcdir}"/refresher/source/pkgs/{betterinlineclock.tar.gz,launchpadPlasma.tar.gz,win7showdesktop-v11-plasma5.18.plasmoid} -t "${pkgdir}/opt/org.koompi.refresher"
    install -Dm744 "${srcdir}/refresher/version.sh" -t "${pkgdir}/var/lib/pix/registry/refresher"
}
