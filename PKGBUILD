pkgname=yandex-browser-beta
pkgver=16.7.0.2846
pkgrel=1
pkgdesc="The web browser from Yandex. / Yandex Browser is a browser that combines a minimal design with sophisticated technology to make the web faster, safer, and easier."
arch=('x86_64')
url="https://browser.yandex.com/"
license=('custom')
options=(!strip)
depends=('desktop-file-utils' 'gconf' 'alsa-lib' 'gtk2' 'libxkbfile' 'nss' 'libxss' 'libxtst')
install='yandex-browser.install'
source=("http://browser.yandex.com/download/?beta=1&os=linux&x64=1&package=deb&full=1")
md5sums=("ca4a012197ed148c978c7cc2076a5d60")

package() {
	cd "$srcdir"
	bsdtar -xfk *.deb -C "${pkgdir}/"
	rm "$pkgdir"/opt/yandex/browser-beta/lib/libffmpeg.so
        rm -r "$pkgdir"/etc
	ln -s /opt/vivaldi/lib/libffmpeg.so "$pkgdir"/opt/yandex/browser-beta/lib/libffmpeg.so
}
