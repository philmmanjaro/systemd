# Maintainer: Philip Müller <philm@manjaro.org>
# Maintainer: Bernhard Landauer <bernhard@manjaro.org>
# Contributor: Christian Hesse <mail@eworm.de>
# Contributor: Dave Reisner <dreisner@archlinux.org>
# Contributor: Tom Gundersen <teg@jklm.no>

pkgbase=systemd
pkgname=('systemd' 'systemd-libs' 'systemd-resolvconf' 'systemd-sysvcompat')
# Can be from either systemd or systemd-stable
_commit='a012f9f7cfc50c88cc6e9630be4aaa829789de02'
pkgver=242.1
pkgrel=1
arch=('x86_64')
url='https://www.github.com/systemd/systemd'
makedepends=('acl' 'cryptsetup' 'docbook-xsl' 'gperf' 'lz4' 'xz' 'pam' 'libelf'
             'intltool' 'iptables' 'kmod' 'libcap' 'libidn2' 'libgcrypt'
             'libmicrohttpd' 'libxslt' 'util-linux' 'linux-api-headers'
             'python-lxml' 'quota-tools' 'shadow' 'gnu-efi-libs' 'git'
             'meson' 'libseccomp' 'pcre2' 'audit' 'kexec-tools' 'libxkbcommon'
             'bash-completion')
options=('strip')
validpgpkeys=('63CDA1E5D3FC22B998D20DD6327F26951A015CC4'  # Lennart Poettering <lennart@poettering.net>
              '5C251B5FC54EB2F80F407AAAC54CA336CFEB557E') # Zbigniew Jędrzejewski-Szmek <zbyszek@in.waw.pl>
source=(# fragment is latest tag for source verification, final merge in prepare()
        "git+https://github.com/systemd/systemd-stable#tag=v${pkgver%.*}?signed"
        "git+https://github.com/systemd/systemd#tag=v${pkgver%.*}?signed"
        '0001-Use-Manjaro-Linux-device-access-groups.patch'
        'initcpio-hook-udev'
        'initcpio-install-systemd'
        'initcpio-install-udev'
        'manjaro.conf'
        'loader.conf'
        'splash-manjaro.bmp'
        'systemd-user.pam'
        'systemd-hook'
        '20-systemd-sysusers.hook'
        '30-systemd-binfmt.hook'
        '30-systemd-catalog.hook'
        '30-systemd-daemon-reload.hook'
        '30-systemd-hwdb.hook'
        '30-systemd-sysctl.hook'
        '30-systemd-tmpfiles.hook'
        '30-systemd-udev-reload.hook'
        '30-systemd-update.hook')
sha512sums=('SKIP'
            'SKIP'
            '764c571f68d092928b9e01c2422bac7c08cc1ac91f969ff2636156c733c81b7cc3f4cd089f8e607a0aad9725751cd52e5fd66c4a8810f16dce6a97906d7fc40a'
            '1f800fe10d1d1c8b1ff45ae352f84dd1918f5559fbf80338b17d490a581ae5e4895c0b51baee7dac9260f4b6f9965da2fa5d33f2a5e31b1afa6c1aafce3e1e49'
            '01de24951a05d38eca6b615a7645beb3677ca0e0f87638d133649f6dc14dcd2ea82594a60b793c31b14493a286d1d11a0d25617f54dbfa02be237652c8faa691'
            'a25b28af2e8c516c3a2eec4e64b8c7f70c21f974af4a955a4a9d45fd3e3ff0d2a98b4419fe425d47152d5acae77d64e69d8d014a7209524b75a81b0edb10bf3a'
            '72dfd0e513e61f391d2b0bf8d9f13c6e2d2732dd7bd52413dccc791c562ab6265062c17d5abe60a42db0775e0b2352eba5e18d14fa2740c176d82edac4867c32'
            '363052706e8fdb040754d0bdc75377212865314ffb8718f8889e6c8a0049ea6cc442cb34fb9a204622eca597b78a547421867cb7517bd1b7342badee581bde7d'
            '6200f2844bdcd230ef4efd27313a92b663a199fe7b3cf1794d17ca4d62bb2d7e9856e6a6e2ea0b912955df124c9d97374c70ae4ef2ff092b25296769fe9e8ba7'
            'b90c99d768dc2a4f020ba854edf45ccf1b86a09d2f66e475de21fe589ff7e32c33ef4aa0876d7f1864491488fd7edb2682fc0d68e83a6d4890a0778dc2d6fe19'
            '869dab2b1837c964add4019bb402e24e52dbb7f009850ca69fcc5deddd923eeb98eb8ee38601f6e31531f30322472fe7df09af84df27f0467708406c55885323'
            '08a590d08043a21f30f04252164b94df972b1ff1022a0469d6aef713e14484a3a037cce290a2a582851e6fac3e64add69d6cc8fc130bbeeaea08626ebf3e1763'
            '5a6b6beef8c31c79018884d948de840f4d3dfb07d9a87081ebf65e2b8fe595bc8c96dbd7742920ccf948c233213ed0026abc913650cefd77ad90c6f8c89bddb8'
            '4cff2ebd962e26e2f516d8b4ac45c839dbfa54dd0588b423c224a328b9f7c62306ca7b2f6cb55240c564caf9972d5bcd2e0efaf2de49d64729aeb3bc1560c9eb'
            '872de70325e9798f0b5a77e991c85bd2ab6de24d9b9ba4e35002d2dd5df15f8b30739a0042a624776177ffc14a838cde7ee98622016ed41df3efda9a659730b2'
            '471342b8d0e05533908cda5d6a906050a51e3181beda1239e91d717029ee40a9eaed714996a445417d87c4e31b7f8522a665de176077fe0536d538369594996d'
            'da783e3bfc6469b92dee4064a13e2b427520d3d96b57c95a4e07aaca3e844d95210a8b16122b022080f5452d65096f274dd1c1467725bbdb2e40ef304b78774a'
            '577e33a1c50b4b41157a67f64162b035dd0c4a541e19cee55a100048bdb50cb2c82852741b1372989a0fe4c4782ba477522747fcc81d72aed99b3db512a86447'
            'e4a9d7607fe93daf1d45270971c8d8455c4bfc2c0bea8bcad05aeb89847edee23cd1a41073a72042622acf417018fe254f5bfc137604fe2c71292680bf67a1c2'
            '209b01b044877cc986757fa4009a92ea98f480306c2530075d153203c3cd2b3afccab6aacc1453dee8857991e04270572f1700310705d7a0f4d5bed27fab8c67')

_backports=(
)

_reverts=(
)

prepare() {
  cd "$pkgbase-stable"

  # add upstream repository for cherry-picking
  git remote add -f upstream ../systemd
  # merge the latest stable commit (fast-foward only to make sure
  # the verified tag is in)
#  git merge --ff-only "${_commit}"

  git checkout "${_commit}"

  local _c
  for _c in "${_backports[@]}"; do
    git log --oneline -1 "${_c}"
    git cherry-pick -n "${_c}"
  done
  for _c in "${_reverts[@]}"; do
    git log --oneline -1 "${_c}"
    git revert -n "${_c}"
  done

  # Replace cdrom/dialout/tape groups with optical/uucp/storage
  patch -Np1 -i ../0001-Use-Manjaro-Linux-device-access-groups.patch
}

pkgver() {
  cd "$pkgbase-stable"

  # TODO: Switch to upstream versioning post v243!

  local _version _count
  _version='v242'
  _count="$(git rev-list --count ${_version}..)"
  printf '%s.%s' "${_version#v}" "${_count}"
}

build() {
  local _timeservers=({0..3}.manjaro.pool.ntp.org)
  local _nameservers=(
    # We use these public name services, ordered by their
    # privacy policy (hopefully):
    #  * Cloudflare (https://1.1.1.1/)
    #  * Quad9 without filtering (https://www.quad9.net/)
    #  * Google (https://developers.google.com/speed/public-dns/)
    1.1.1.1
    9.9.9.10
    8.8.8.8
    2606:4700:4700::1111
    2620:fe::10
    2001:4860:4860::8888
  )

  local _meson_options=(
    -Dversion-tag="${pkgver}-${pkgrel}-manjaro"

    -Dgnu-efi=true
    -Dima=false
    -Dlibidn2=true
    -Dlz4=true
    -Dman=true

    -Ddbuspolicydir=/usr/share/dbus-1/system.d
    -Ddefault-hierarchy=hybrid
    -Ddefault-locale=C
    -Ddefault-kill-user-processes=false
    -Dfallback-hostname='manjaro'
    -Dntp-servers="${_timeservers[*]}"
    -Ddns-servers="${_nameservers[*]}"
    -Drpmmacrosdir=no
    -Dsysvinit-path=
    -Dsysvrcnd-path=
    -Dsupport-url='https://forum.manjaro.org/c/technical-issues-and-assistance'
  )

  arch-meson "$pkgbase-stable" build "${_meson_options[@]}"

  ninja -C build
}

#check() {
#  meson test -C build
#}

package_systemd() {
  pkgdesc='system and service manager'
  license=('GPL2' 'LGPL2.1')
  depends=('acl' 'bash' 'cryptsetup' 'dbus' 'iptables' 'kbd' 'kmod' 'hwids' 'libcap'
           'libgcrypt' 'systemd-libs' 'libidn2' 'libidn2.so' 'lz4' 'pam' 'libelf'
           'libseccomp' 'util-linux' 'xz' 'pcre2' 'audit')
  provides=('nss-myhostname' "systemd-tools=$pkgver" "udev=$pkgver")
  replaces=('nss-myhostname' 'systemd-tools' 'udev')
  conflicts=('nss-myhostname' 'systemd-tools' 'udev')
  optdepends=('libmicrohttpd: remote journald capabilities'
              'quota-tools: kernel-level quota management'
              'systemd-sysvcompat: symlink package to provide sysvinit binaries'
              'polkit: allow administration as unprivileged user'
              'curl: machinectl pull-tar and pull-raw')
  backup=(etc/pam.d/systemd-user
          etc/systemd/coredump.conf
          etc/systemd/journald.conf
          etc/systemd/journal-remote.conf
          etc/systemd/journal-upload.conf
          etc/systemd/logind.conf
          etc/systemd/networkd.conf
          etc/systemd/resolved.conf
          etc/systemd/sleep.conf
          etc/systemd/system.conf
          etc/systemd/timesyncd.conf
          etc/systemd/user.conf
          etc/udev/udev.conf)
  install=systemd.install

  DESTDIR="$pkgdir" meson install -C build

  # only in v242
  # don't write units to /etc by default. some of these will be re-enabled on
  # post_install.
  if [ -e "$pkgdir"/etc/systemd/system/ ]; then
      rm -rv "$pkgdir"/etc/systemd/system/*
  fi

  # we'll create this on installation
  rmdir "$pkgdir"/var/log/journal/remote

  # runtime libraries shipped with systemd-libs
  install -d -m0755 systemd-libs
  mv "$pkgdir"/usr/lib/lib{nss,systemd,udev}*.so* systemd-libs

  # manpages shipped with systemd-sysvcompat
  rm "$pkgdir"/usr/share/man/man8/{halt,poweroff,reboot,runlevel,shutdown,telinit}.8

  # executable (symlinks) shipped with systemd-sysvcompat
  rm "$pkgdir"/usr/bin/{halt,init,poweroff,reboot,runlevel,shutdown,telinit}

  # files shipped with systemd-resolvconf
  rm "$pkgdir"/usr/{bin/resolvconf,share/man/man1/resolvconf.1}

  if [ -e "$pkgdir"/usr/share/factory/etc/issue ]; then
      # only in v243
      # avoid a potential conflict with [core]/filesystem
      rm "$pkgdir"/usr/share/factory/etc/{issue,nsswitch.conf}
      sed -i -e '/^C \/etc\/nsswitch\.conf/d' \
       -e '/^C \/etc\/issue/d' "$pkgdir"/usr/lib/tmpfiles.d/etc.conf
  else
      # only in v242
      # avoid a potential conflict with [core]/filesystem
      rm "$pkgdir"/usr/share/factory/etc/nsswitch.conf
      sed -i '/^C \/etc\/nsswitch\.conf/d' "$pkgdir"/usr/lib/tmpfiles.d/etc.conf
  fi

  # add back tmpfiles.d/legacy.conf, normally omitted without sysv-compat
  install -m0644 $pkgbase-stable/tmpfiles.d/legacy.conf "$pkgdir"/usr/lib/tmpfiles.d

  # ship default policy to leave services disabled
  echo 'disable *' >"$pkgdir"/usr/lib/systemd/system-preset/99-default.preset

  # add mkinitcpio hooks
  install -D -m0644 initcpio-install-systemd "$pkgdir"/usr/lib/initcpio/install/systemd
  install -D -m0644 initcpio-install-udev "$pkgdir"/usr/lib/initcpio/install/udev
  install -D -m0644 initcpio-hook-udev "$pkgdir"/usr/lib/initcpio/hooks/udev

  # ensure proper permissions for /var/log/journal
  # The permissions are stored with named group by tar, so this works with
  # users and groups populated by systemd-sysusers. This is only to prevent a
  # warning from pacman as permissions are set by systemd-tmpfiles anyway.
  install -d -o root -g systemd-journal -m 2755 "$pkgdir"/var/log/journal

  # match directory owner/group and mode from [extra]/polkit
  install -d -o root -g 102 -m 0750 "$pkgdir"/usr/share/polkit-1/rules.d

  # add example bootctl configuration
  install -D -m0644 manjaro.conf "$pkgdir"/usr/share/systemd/bootctl/manjaro.conf
  install -D -m0644 loader.conf "$pkgdir"/usr/share/systemd/bootctl/loader.conf
  install -D -m0644 splash-manjaro.bmp "$pkgdir"/usr/share/systemd/bootctl/splash-manjaro.bmp

  # pacman hooks
  install -D -m0755 systemd-hook "$pkgdir"/usr/share/libalpm/scripts/systemd-hook
  install -D -m0644 -t "$pkgdir"/usr/share/libalpm/hooks *.hook

  # overwrite the systemd-user PAM configuration with our own
  install -D -m0644 systemd-user.pam "$pkgdir"/etc/pam.d/systemd-user
}

package_systemd-libs() {
  pkgdesc='systemd client libraries'
  depends=('glibc' 'libcap' 'libgcrypt' 'lz4' 'xz')
  license=('LGPL2.1')
  provides=('libsystemd' 'libsystemd.so' 'libudev.so')
  conflicts=('libsystemd')
  replaces=('libsystemd')

  install -d -m0755 "$pkgdir"/usr
  mv systemd-libs "$pkgdir"/usr/lib
}

package_systemd-resolvconf() {
  pkgdesc='systemd resolvconf replacement (for use with systemd-resolved)'
  license=('LGPL2.1')
  depends=('systemd')
  provides=('openresolv' 'resolvconf')
  conflicts=('openresolv')

  install -d -m0755 "$pkgdir"/usr/bin
  ln -s resolvectl "$pkgdir"/usr/bin/resolvconf

  install -d -m0755 "$pkgdir"/usr/share/man/man1
  ln -s resolvectl.1.gz "$pkgdir"/usr/share/man/man1/resolvconf.1.gz
}

package_systemd-sysvcompat() {
  pkgdesc='sysvinit compat for systemd'
  license=('GPL2')
  conflicts=('sysvinit')
  depends=('systemd')

  install -D -m0644 -t "$pkgdir"/usr/share/man/man8 \
    build/man/{telinit,halt,reboot,poweroff,runlevel,shutdown}.8

  install -d -m0755 "$pkgdir"/usr/bin
  ln -s ../lib/systemd/systemd "$pkgdir"/usr/bin/init
  for tool in runlevel reboot shutdown poweroff halt telinit; do
    ln -s systemctl "$pkgdir"/usr/bin/$tool
  done
}

# vim:ft=sh syn=sh et sw=2:
