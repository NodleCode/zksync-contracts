# ZkSync Contracts (compatible with foundry)
A simple repo to ensure the ZkSync Contracts ([github](https://github.com/matter-labs/era-contracts), [npm](https://www.npmjs.com/package/@matterlabs/zksync-contracts)) are usable with `forge` fropm `foundry`.

## Methodology
The contracts in the github repo are __templates__ which are generated and prefilled when pushed to NPM. However `forge` does not support NPM packages, as such we fetched the raw content of the ZkSync NPM packages and dump it here in github where it can be `forge install`'d!

## Updating
Download the tarball available via `npm view @matterlabs/zksync-contracts dist.tarball`, decompress it.

ie:
```sh
rm -rf l1 l2 && \
    curl -o contracts.tar.gz `npm view @matterlabs/zksync-contracts dist.tarball` && \
    tar -xzf contracts.tar.gz && \
    rm contracts.tar.gz && \
    mv package/l2 . && \
    mv package/l1 . && \
    rm -rf package
```