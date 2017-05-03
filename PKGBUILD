pkgbasename=python-kwalify
pkgname=(python2-kwalify python-kwalify)
pkgver=1.6.0
pkgrel=1
pkgdesc="Python YAML/JSON validation library"
arch=('i686' 'x86_64')
url="https://github.com/Grokzen/pykwalify"
license=('MIT')
makedepends=('python' 'python2')
source=(https://github.com/Grokzen/pykwalify/releases/download/${pkgver}/pykwalify-${pkgver}.tar.gz)
sha256sums=('97f880ccf5de3b50f85d08226333e4474fcb1ede8d76438e7a6df0831cf0d95d')

build() {
	cd "${srcdir}"
	cp -r "pykwalify-${pkgver}" "python2-kwalify-${pkgver}"
}

package_python2-kwalify() {
    depends=('python2' 'python2-yaml' 'python2-dateutil' 'python2-docopt')
    cd "${srcdir}/python2-kwalify-${pkgver}"
    python2 setup.py install --root="${pkgdir}/" --optimize=1
}

package_python-kwalify() {
    depends=('python' 'python-yaml' 'python-dateutil' 'python-docopt')
    cd "${srcdir}/pykwalify-${pkgver}"
    python3 setup.py install --root="${pkgdir}/" --optimize=1
}
