# Contributor: Richard Macwan <rich4rd.macwan@gmail.com>
pkgname=youtube-dl-audio
pkgver=0.1.0
pkgrel=1
pkgdesc="A convenience bash script based on youtube-dl to download audio directly"
url="https://code.google.com/p/time-lapse"
arch=('i686' 'x86_64')
license="GPLv3"
depends=('bash')
makedepends=(git)
_gitroot="https://code.google.com/p/youtube-dl-audio/"
_gitname="youtube-dl-audio"
md5sums=()
build()
{
    cd ${srcdir}/

    msg "Connecting to the GIT server...."
    if [[ -d ${srcdir}/${_gitname} ]] ; then
        cd ${_gitname}
        git pull origin
        msg "The local files are updated..."
    else
    msg "Cloning ..."
        git clone ${_gitroot}
    fi
    
    msg "GIT checkout done."
    cp $srcdir/$pkgname/src/$pkgname "$pkgdir/usr/bin/"

}
package() {
make 
#install -Dm644 $srcdir/$pkgname/src/$pkgname "$pkgdir/usr/bin/"
}