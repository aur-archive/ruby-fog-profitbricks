# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=fog-profitbricks
pkgname=ruby-$_gemname
pkgver=0.0.1
pkgrel=1
pkgdesc='Module for the '\''fog'\'' gem to support ProfitBricks.'
arch=(any)
url='https://github.com/fog/fog-profitbricks'
license=(MIT)
depends=(ruby ruby-fog-core ruby-fog-xml ruby-nokogiri)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('fe8051fc89456d7e3318245e1efe7fc81945f4da')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
