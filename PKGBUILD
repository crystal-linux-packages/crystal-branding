# Maintainer:  echo -n 'bWljaGFsQGdldGNyeXN0LmFs'     | base64 -d
# Contributor: echo -n 'bWF0dEBnZXRjcnlzdC5hbA=='     | base64 -d
# Contributor: echo -n 'cmNhbmRhdUBnZXRjcnlzdC5hbA==' | base64 -d

pkgname=crystal-branding
_pkgname=branding
pkgver=2022.10.08
pkgrel=2
pkgdesc='Crystal Linux branding'
arch=('any')
url="https://github.com/crystal-linux/${_pkgname}"
license=('GPL3')
depends=('lsb-release')
install="${pkgname}.install"
source=("${pkgname}-${pkgver}::${url}/archive/${pkgver}.tar.gz"
	"os-release_crystal"
	"issue_crystal"
	"lsb-release_crystal")
sha256sums=('8e39286724310ca566fc02908e83456bd15d4fa102addd12f8c9c8fad8eeddd4'
	    '7b284f8f71a0cc9943b0b68dec694dc6f314ec779c0dca23c84d02d271a02725'
	    'af9064feb584990461d65dc4810aec4395754924b3fea564b84b8d76d47538f6'
	    '2bd31d1d5dcc0ce320c288ffe62f1e87cb5705d041825fb0f104425f7a10991f')

package () {
    cd "${srcdir}/${_pkgname}-${pkgver}"
    install -Dm 644 in-system/crystal-os-logo.png "${pkgdir}/usr/share/pixmaps/crystal-os-logo.png"
    install -Dm 644 ../os-release_crystal "${pkgdir}/etc/os-release_crystal"
    install -Dm 644 ../os-release_crystal "${pkgdir}/usr/lib/os-release/os-release_crystal"
    install -Dm 644 ../issue_crystal "${pkgdir}/etc/issue_crystal"
    install -Dm 644 ../lsb-release_crystal "${pkgdir}/etc/lsb-release_crystal"
}
