# Maintainer: Eric Mertens <emertens@gmail.com>

pkgname=biosdisk
pkgver=0.6.1.1.2
pkgrel=1
arch=('i686' 'x86_64')
pkgdesc="Dell BIOS Flash disk image creation"
url="http://linux.dell.com/biosdisk/"
license=("GPL")
depends=('syslinux' 'hd2u' 'python' 'wget')
makedepends=('gcc')
md5sums=('fc5d08cf341683dd1e52d3fd0a51b3c4')
source=(http://linux.dell.com/biosdisk/biosdisk-git-06112010.tar.gz)

build()
{
  cd $startdir/src/$pkgname-$pkgver

  mkdir -p $startdir/pkg/etc
  mkdir -p $startdir/pkg/usr/man/man8
  mkdir -p $startdir/pkg/usr/sbin
  mkdir -p $startdir/pkg/usr/share/biosdisk
  mkdir -p $startdir/pkg/var/lib/biosdisk

  install -m 755 biosdisk $startdir/pkg/usr/sbin
  install -m 755 blconf $startdir/pkg/usr/sbin
  install -m 644 dosdisk.img $startdir/pkg/usr/share/biosdisk
  install -m 644 biosdisk.conf $startdir/pkg/etc
  install -m 644 biosdisk-mkrpm-redhat-template.spec $startdir/pkg/usr/share/biosdisk
  install -m 644 biosdisk-mkrpm-generic-template.spec $startdir/pkg/usr/share/biosdisk
  install -m 644 biosdisk.8.gz $startdir/pkg/usr/man/man8
}
