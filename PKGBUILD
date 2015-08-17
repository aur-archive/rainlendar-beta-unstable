# Contributor: Ng Oon-Ee <ngoonee.talk@gmail.com>
# Based on rainlendar-beta by Blasse <koralik(at)gmail(dot)com>
pkgname=rainlendar-beta-unstable
pkgver=2.12.b130
pkgrel=1
if [ "${CARCH}" = 'i686' ]; then
  source=(http://www.rainlendar.net/download/Rainlendar-$pkgver-i386.tar.bz2)
  md5sums=('82aa1d2bcb2c17dfa3403a874a511482')
else
  source=(http://www.rainlendar.net/download/Rainlendar-$pkgver-amd64.tar.bz2)
  md5sums=('3b668f62b629ba31caee7716abfeab3e')
fi

pkgdesc="A desktop Calendar, ToDo list and Event list. An unstable (untested) beta version."
arch=('i686' 'x86_64')
url="http://www.rainlendar.net"
license=('custom')
depends=('cairo' 'libsm' 'expat>=1.95.8' 'libstdc++5' 'libpng12' 'openssl098')
conflicts=('rainlendar-lite' 'rainlendar-beta')

package() {
  install -d "${pkgdir}/opt" "${pkgdir}/usr/bin" "${pkgdir}/usr/share/licenses/${pkgname}"

  cp -R "${srcdir}/rainlendar2" "${pkgdir}/opt"
  ln -s "/opt/rainlendar2/rainlendar2" "${pkgdir}/usr/bin/rainlendar"
  ln -s "/opt/rainlendar2/License.txt" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
