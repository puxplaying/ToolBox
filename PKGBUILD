# Maintainer: Chrysostomus @forum.manjaro.org
# Maintainer: puxplaying

pkgname=bmenu
pkgver=0.9
pkgrel=1
pkgdesc="Bash scripts providing a collection of terminal applications in a simple UI"
arch=(any)
url="https://github.com/puxplaying/toolbox/" # By changing this to "https://github.com/$YourAccount/toolbox" you should be able to release packages on your Github fork!
license=('GPL3')
depends=('pacui' 'pacman-contrib' 'expac' 'sudo' 'fzf' 'ncdu' 'gawk' 'bash' 'links' 'sed' 'xorg-xinput' 'inxi' 'cpupower' 'ranger' 'curl' 'powertop' 'cmus' 'mhwd' 'lshw' 'lm_sensors' 'dmidecode')
makedepends=('git')
conflicts=("mhwd-tui")
provides=("mhwd-tui")
optdepends=('cmatrix: Needed for ToolBox'
			'meld: Needed for diff operations')
source=("$url/archive/$pkgver.tar.gz")
md5sums=('SKIP')

package () {
	cd "$srcdir/toolbox-$pkgver"
	install -dm755 $pkgdir/usr/bin
	cp -r $srcdir/toolbox-$pkgver/bin $pkgdir/usr
	#chmod a+x $pkgdir/usr/bin/* # All included scripts should already be set to executable (We can't chmod a symlink)
}
