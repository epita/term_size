# How to update the AUR

- Update `term_size`
- ```bash
mkdir term_size
cp ../term_size term_size
tar cvf term_size-<version>.tar.gz term_size/term_size # Change <version> to the appropriate version
openssl md5 term_size-<version>.tar.gz
```
- Update PKGBUILD's version and MD5 checksum from previous command
- ```bash
makepkg --printsrcinfo > .SRCINFO
```
- Update AUR's repository with:
    - The new *.tar.gz
    - The updated .SRCINFO
    - The updated PKGBUILD

