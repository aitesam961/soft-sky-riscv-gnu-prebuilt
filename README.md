# soft-sky
Up-to-date Prebuilt RISCV GNU toolchain for painless setup. No more build from source everytime.



This repository makes use of GitHub actions to build the `riscv-gnu-toolchain` from source. Just download the prebuilt binaries, add to path and use.

### Installation
- Download the prebuilt binaries from GitHub Actions > Artifacts
- Create directory in the root e.g `/tools/riscv` or `/opt/riscv`. Requried `sudo`
```
$ sudo mkdir /tools/riscv
```
- Extract the downloaded file and paste in newly created directory.
```
$ sudo tar -xzf riscv-toolchain.tar.gz -C /tools/riscv/
```
- Add to your system environment variables
```
$ export PATH=$PATH:/tools/riscv/bin
```
### Verify installation 
Run the following Command
```
$ riscv64-unknown-elf-gcc -v

Using built-in specs.
COLLECT_GCC=riscv64-unknown-elf-gcc
COLLECT_LTO_WRAPPER=/usr/lib/gcc/riscv64-unknown-elf/10.2.0/lto-wrapper
Target: riscv64-unknown-elf
Configured with: ../configure --build=x86_64-linux-gnu
...
```
### TODO:

- [ ] Build for both `newlib` and `linux` toolchains
- [ ] Trigger rebuild upon new release from source to stay up to date.
- [ ] Multiple extensions and variants support
