# Maintainer: Julien Nicoulaud <julien.nicoulaud@gmail.com>
_pkgname=drone-runner-exec
_pkgver=1.0.0-beta.9
pkgver=${_pkgver//-/.}
pkgname=${_pkgname}-bin
pkgrel=2
pkgdesc="Drone pipeline runner that executes builds directly on the host machine."
arch=('x86_64' 'i686' 'armv7h' 'aarch64')
url="https://github.com/drone-runners/drone-runner-exec"
license=('Polyform-Small-Business-1.0.0' 'Polyform-Free-Trial-1.0.0')
provides=("${_pkgname}")
conflicts=("${_pkgname}" "${_pkgname}-git")
backup=("etc/drone-runner-exec/config")
source_x86_64=("https://github.com/drone-runners/${_pkgname}/releases/download/v${_pkgver}/drone_runner_exec_linux_amd64.tar.gz")
source_i686=("https://github.com/drone-runners/${_pkgname}/releases/download/v${_pkgver}/drone_runner_exec_linux_386.tar.gz")
source_armv7h=("https://github.com/drone-runners/${_pkgname}/releases/download/v${_pkgver}/drone_runner_exec_linux_arm.tar.gz")
source_aarch64=("https://github.com/drone-runners/${_pkgname}/releases/download/v${_pkgver}/drone_runner_exec_linux_arm64.tar.gz")
source=("https://polyformproject.org/wp-content/uploads/2020/05/PolyForm-Small-Business-1.0.0.txt"
        "https://polyformproject.org/wp-content/uploads/2020/05/PolyForm-Free-Trial-1.0.0.txt")
sha512sums_x86_64=('e92063fa96191d1d8b1d3a36885efaf8b54251e10e972efbba49949b7d094e0cb1ddaec419baacd7a8743aacf4c9d7858344a0d35b5b4e16dfa1ccaa52d82cb9')
sha512sums_i686=('2fb21f9d97e977998dc98283588094398fd4e0e1d1ff2a5873d3cea53dd1551c66fd3b197025bdc32369504158260b72c7232b3a6ffb0cd800789731873d1f4e')
sha512sums_armv7h=('df840ff4a15602177e400a6a38bf10466a9838edf0a11d7458fd061d9548f5a48265e48c79b49607d9a87ea82dc70d75c2a9922484208ace8dbd49842ace4810')
sha512sums_aarch64=('110a2ca56fedd19e83ab896da6ee4a190dc5b5db8f9813e945fc34c5129657345808e704e06ea06486f6bc51a46a9dd732da76c09eb573929edd8ff549ad9ede')
sha512sums=('34514288fd78afcc21b86ff5d23dc0e4ccc8dc67d2db032480a3cfb89de5ad9bb19370cad8049a104fa3d44b5e03c208dc8425aa24bcd7e763c3673c7514beb6'
            '66e97a91ce27f2711a102f47660fc407b0fdde35564c64ab3c2fae55cbdb3fadf957cafcb0b19c6be94d6a2336cbfb92ee2d8ecf58c8ef627ba601e7bfadcee0')

package() {
  cd "${srcdir}"
  install -Dm 755 "${_pkgname}" "${pkgdir}/usr/bin/${_pkgname}"
  install -Dm 644 "PolyForm-Small-Business-1.0.0.txt" "${pkgdir}/usr/share/licenses/${pkgname}/PolyForm-Small-Business-1.0.0.txt"
  install -Dm 644 "PolyForm-Free-Trial-1.0.0.txt" "${pkgdir}/usr/share/licenses/${pkgname}/PolyForm-Free-Trial-1.0.0.txt"
}
