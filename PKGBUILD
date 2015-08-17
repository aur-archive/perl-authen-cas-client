# Generated by Xyne::Arch::CPAN 0.07

pkgname=perl-authen-cas-client
pkgver=0.06
pkgrel=1
pkgdesc="Provides an easy-to-use interface for authentication using JA-SIG's Central Authentication Service"
arch=('i686' 'x86_64')
url="http://search.cpan.org/dist/Authen-CAS-Client/"
license=('BSD')
source=('http://search.cpan.org/CPAN/authors/id/P/PR/PRAVUS/Authen-CAS-Client-0.06.tar.gz')
md5sums=('e8673e8c30e76b0bf14a5a804355f2d8')
depends=('perl-libwww>=6.02' 'perl-uri' 'perl-xml-libxml' 'perl>=5.6.1')
makedepends=('perl-extutils-makemaker>=6.42' 'perl-test-mockobject>=0.00')
provides=('perl-authen-cas-client-response=0.03')
options=(!emptydirs)

build() {
  _dir=$(find $srcdir -maxdepth 2 -type f -name 'Makefile.PL')
  if [ ! -z "$_dir" ]; then
    cd $(dirname "$_dir")
    PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor || return 1
    make  || return 1
    make install DESTDIR="${pkgdir}" || return 1

  else
  _dir=$(find $srcdir -maxdepth 2 -type f -name 'Build.PL')
  if [ ! -z "$_dir" ]; then
    cd $(dirname "$_dir")
    PERL_MM_USE_DEFAULT=1 perl Build.PL INSTALLDIRS=vendor || return 1
    ./Build  || return 1
    ./Build install destdir=${pkgdir} || return 1

  else
    echo "error: failed to detect build method for $pkgname"
    echo "you may be able to fix this by editing the PKGBUILD"
    return 1
  fi fi

  # remove perllocal.pod and .packlist
  find ${pkgdir} -name perllocal.pod -delete
  find ${pkgdir} -name .packlist -delete
}

# vim:set ts=2 sw=2 et:

