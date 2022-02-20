# Void Linux template for Nody Greeter

This is the template for [nody-greeter][nody-greeter], made for automatic building through github workflows. You can get the latest xbps packages inside the **Actions** tabpage, or at the latest release in nody-greeter repo.

> Note: Xbps packages in the main repo not yet available

## Build

Instructions to build `nody-greeter` with `xbps-src`:

1. Setup `void-packages`:

```sh
git clone --depth=1 https://github.com/void-linux/void-packages
cd void-packages
./xbps-src binary-bootstrap
```

2. Download this repo and copy to `srcpkgs`:

```sh
git clone https://github.com/JezerM/nody-greeter-void
mv nody-greeter-void ./srcpkgs/nody-greeter
```

3. Build and install:

```sh
./xbps-src pkg nody-greeter
sudo xbps-install --repository=hostdir/binpkgs nody-greeter
```

[nody-greeter]: https://github.com/JezerM/nody-greeter "Nody Greeter"
