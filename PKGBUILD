# Maintainer: Czipperz <czipperz@gmail.com>

pkgname=oh-my-zsh-local
pkgver=1.0
pkgrel=1
pkgdesc="Downloads oh-my-zsh from git and installs it in the local directory"
arch=('any')
license=('GPL3')
depends=('zsh')
makedepends=('git')
url="https://github.com/robbyrussell/oh-my-zsh"

package() {
	cd $HOME
	echo "Cloning the git repo into $HOME/.oh-my-zsh"
	git clone git://github.com/robbyrussell/oh-my-zsh.git .oh-my-zsh
	echo "Attempting to backup your .zshrc file into $HOME/.zshrc.orig"
	mv .zshrc .zshrc.orig
	echo "Copying the template for the config file into $HOME/.zshrc"
	cp .oh-my-zsh/templates/zshrc.zsh-template .zshrc
	echo "Changing default shell for you:"
	chsh -s /bin/zsh
}
