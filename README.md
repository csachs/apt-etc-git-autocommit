# apt-etc-git-autocommit

The `/etc` directory often drifts considerably over time, sometimes making it unclear when and why certain changes appeared later on. This two-line apt hook just stores everything into a git repository in `/etc` (`/etc/.git`) automatically. Beware, this includes sensitive files like `/etc/shadow`… permissions are set to `600` for the `.git` repository to prevent other users from accessing it, but I have not deeply investigated the security of this approach. Use at your own risk and with special care, particularly in multi-user systems.

## Installation 

```bash
sudo wget https://github.com/csachs/apt-etc-git-autocommit/releases/download/v1.0-1/apt-etc-git-autocommit_1.0-1.deb
sudo apt install ./apt-etc-git-autocommit_1.0-1.deb
```

## Building

```bash
dpkg-deb --build apt-etc-git-autocommit_1.0-1
```

## See also

This two-liner is a minimal approach the topic, if you want a more full-featured solution, check out [etckeeper](https://github.com/wertarbyte/etckeeper).

## License

CC-0

