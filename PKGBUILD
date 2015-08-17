# Maintainer: Jon Eyolfson <jon@eyolfson.com>

pkgname=python2-django-celery
_pypi_pkgname=django-celery
pkgver=3.0.11
pkgrel=3
pkgdesc="Celery integration for Django"
url="http://celeryproject.org/"
license=('BSD')
arch=('any')
makedepends=('python2' 'python2-distribute')
depends=('python2-celery' 'python2-pytz')
source=(http://pypi.python.org/packages/source/d/${_pypi_pkgname}/${_pypi_pkgname}-${pkgver}.tar.gz)
md5sums=('2861a1074ebb7608de2eab883097781f')
 
build() {
  cd "${srcdir}/${_pypi_pkgname}-${pkgver}"  
  python2 setup.py build
}

package() {
  cd "${srcdir}/${_pypi_pkgname}-${pkgver}"
  python2 setup.py install --root="${pkgdir}" --optimize=1
  install -D -m644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
