# testrepofork

https://www.phusionpassenger.com/library/walkthroughs/deploy/ruby/ownserver/nginx/oss/install_language_runtime.html

sudo apt-get update
sudo apt-get install -y curl gnupg build-essential

#gpgv2 install following the error message
gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
curl -sSL https://get.rvm.io | bash -s stable

root@3f917b6b9bb5:/sample_rails_app/config/environments# curl -sSL https://get.rvm.io | bash -s stable
Downloading https://github.com/rvm/rvm/archive/1.29.10.tar.gz
Downloading https://github.com/rvm/rvm/releases/download/1.29.10/1.29.10.tar.gz.asc
gpg: Signature made Wed Mar 25 21:58:42 2020 UTC
gpg:                using RSA key 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
gpg: Good signature from "Piotr Kuczynski <piotr.kuczynski@gmail.com>" [unknown]
gpg: WARNING: This key is not certified with a trusted signature!
gpg:          There is no indication that the signature belongs to the owner.
Primary key fingerprint: 7D2B AF1C F37B 13E2 069D  6956 105B D0E7 3949 9BDB
GPG verified '/usr/local/rvm/archives/rvm-1.29.10.tgz'
Creating group 'rvm'
Installing RVM to /usr/local/rvm/
Installation of RVM in /usr/local/rvm/ is almost complete:

  * First you need to add all users that will be using rvm to 'rvm' group,
    and logout - login again, anyone using rvm will be operating with `umask u=rwx,g=rwx,o=rx`.

  * To start using RVM you need to run `source /etc/profile.d/rvm.sh`
    in all your open shell windows, in rare cases you need to reopen all shell windows.
  * Please do NOT forget to add your users to the rvm group.
     The installer no longer auto-adds root or users to the rvm group. Admins must do this.
     Also, please note that group memberships are ONLY evaluated at login time.
     This means that users must log out then back in before group membership takes effect!
  * WARNING:  version This account is currently not available. detected - Zsh 4.3.12 / 5.0.0+ is recommended,
     with current one errors to be expected - bugs in shell code interpretation.
Thanks for installing RVM 🙏
Please consider donating to our open collective to help us maintain RVM.

👉  Donate: https://opencollective.com/rvm/donate

root@3f917b6b9bb5:~# export PATH=$PATH:/usr/local/rvm/bin
root@3f917b6b9bb5:~# which rvm
/usr/local/rvm/bin/rvm
root@3f917b6b9bb5:~# rvm --version
rvm 1.29.10 (latest) by Michal Papis, Piotr Kuczynski, Wayne E. Seguin [https://rvm.io]
root@3f917b6b9bb5:~# rvm install ruby
Searching for binary rubies, this might take some time.
Found remote file https://rvm_io.global.ssl.fastly.net/binaries/ubuntu/20.04/x86_64/ruby-2.7.0.tar.bz2
Checking requirements for ubuntu.
Installing requirements for ubuntu.
Updating system..
Installing required packages: gawk, autoconf, automake, bison, libffi-dev, libgdbm-dev, libncurses5-dev, libsqlite3-dev, libtool, libyaml-dev, pkg-config, sqlite3, zlib1g-dev, libgmp-dev, libreadline-dev, libssl-dev
Requirements installation successful.
ruby-2.7.0 - #configure
ruby-2.7.0 - #download
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 21.3M  100 21.3M    0     0  6291k      0  0:00:03  0:00:03 --:--:-- 6293k
No checksum for downloaded archive, recording checksum in user configuration.
ruby-2.7.0 - #validate archive
ruby-2.7.0 - #extract
ruby-2.7.0 - #validate binary
ruby-2.7.0 - #setup
ruby-2.7.0 - #gemset created /usr/local/rvm/gems/ruby-2.7.0@global
ruby-2.7.0 - #importing gemset /usr/local/rvm/gemsets/global.gems..................................
ruby-2.7.0 - #generating global wrappers.......
ruby-2.7.0 - #gemset created /usr/local/rvm/gems/ruby-2.7.0
ruby-2.7.0 - #importing gemsetfile /usr/local/rvm/gemsets/default.gems evaluated to empty gem list
ruby-2.7.0 - #generating default wrappers.......
root@3f917b6b9bb5:~#

root@3f917b6b9bb5:/sample_rails_app# useradd -m -d /home/deploy -s /bin/bash -c "Donisha Deploy" -U deploy
root@3f917b6b9bb5:/sample_rails_app# su deploy
deploy@3f917b6b9bb5:/sample_rails_app$ exit
exit
root@3f917b6b9bb5:/sample_rails_app#


