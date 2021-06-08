# Just some useful linux commands and scripts

#### Recursively change directory or file permissions

Directories

```shell
sudo find /path -type d -exec chmod 755 {} + 
```

Files

```shell
sudo find /path -type f -exec chmod 755 {} + 
```

#### Recursively all node_modules, build, .cache directories

_useful before running a backup or copying across the network_

```shell
alias delete-node-modules='cd ~/repos ; find . -name "node_modules" -type d -prune -exec rm -rf '{}' +'

alias delete-build='cd ~/repos ; find . -name "build" -type d -prune -exec rm -rf '{}' +'

alias delete-cache='cd ~/repos ; find . -name ".cache" -type d -prune -exec rm -rf '{}' +'
```

#### GPG

```shell
gpg --full-generate-key 

gpg --list-secret-keys --keyid-format LONG 
gpg --list-keys 

gpg --armor --export <KEY ID>
gpg --export-secret-keys -o secring.kbx
gpg --export-secret-key <KEY ID> > secring.gpg 

gpg --keyserver hkp://keyserver.ubuntu.com/ --send-keys <KEY ID> 
#retrieve key(s) from key server 
gpg --recv-key <KEY_ID> <KEY_ID_2>
```

#### rsync

```shell
#rsync using ssh with key
rsync -avz -e "ssh -i /path/.ssh/id_rsa" --progress source user@55.55.55.55:~
```