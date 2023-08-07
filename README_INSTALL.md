# Install RISC-V Toolchain

If you do not have look with gdb-multiarch, e.g. because it does not step into kernel using "stepi" on ecall instruction, you might have to install the riscv-gnu-toolchain.

```console
git clone --recursive https://github.com/riscv/riscv-gnu-toolchain
cd riscv-gnu-toolchain
./configure --prefix=/usr/local
sudo make
cd ..
```

To be able to use the .gdbinit failed contained in this folder,
one must allow it in ~/.gdbinit.

To get the c_cpp_properties.json

```console
make clean && bear -- make qemu
```