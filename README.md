mingos yum repository
====

## Description
Original RPM repository for CentOS

## Usage

### create /etc/yum.repos.d/mingos.repo

```sh
$ sudo cat << 'EOF' | sudo tee /etc/yum.repos.d/mingos.repo
[mingos]
name=mingos
baseurl=https://mingos.github.io/yumrepo/el7/x86_64/
enabled=1
gpgcheck=0
EOF
```

### list RPM packages

```sh
$ yum list |grep mingos
mecab.x86_64                                0.996-1                    @mingos
mecab-ipadic.x86_64                         2.7.0_20070801-1           @mingos
tig.x86_64                                  2.2-1                      @mingos
...
```

### install pakage

```sh
$ sudo yum -y install tig
```

## Licence

[MIT](https://github.com/tcnksm/tool/blob/master/LICENCE)

## Author

[mingos](https://github.com/mingos)

