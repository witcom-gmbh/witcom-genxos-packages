# witcom-genxos-packages

## Build

Exemplarisch für witcom-genxos-helper 

```
mkdir ./bin
docker run --rm -v "$(pwd)"/bin/:/home/build/openwrt/bin -it openwrtorg/sdk:kirkwood-generic-21.02.3
#ab jetzt im container
cd /tmp
git@github.com:witcom-gmbh/witcom-genxos-packages.git
cd -
cp /tmp/witcom-genxos-packages/witcom-genxos-helper/diffconfig .config
./scripts/feeds update base
make defconfig
cp -rf /tmp/witcom-genxos-packages/witcom-genxos-helper package/
make package/witcom-genxos-helper/compile -j$(nproc)
exit
```

Das erzeugt Pakete liegt dann unter ./bin
