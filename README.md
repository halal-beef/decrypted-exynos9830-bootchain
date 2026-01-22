# Decrypted parts of the Exynos 9830 (990) bootchain

I'll start this off with a notice, do not expect these to work if sent under hubble,
the decrypted parts of the bootchain will not pass the integrity checks, this is just
for anyone who wants to do firmware analysis.

As of right now the only dump available is from G981BXXSMHXK1, taken from my personal
Samsung Galaxy S20 5G using an exploit to dump each stage.

Only EPBL and EL3_MONITOR are encrypted but for the sake of being able to have a look
at the other stages, i've included other binaries in the folder too.

## Loading the stages into Ghidra

ALL stages should be loaded with AARCH64 V8A LE DEFAULT. Though, load addresses differ.

FWBL1 / BL1 is loaded at ```0x02022000```

EPBL is loaded at ```0x02026000```

BL2 is loaded at ```0x15600000```

LK is loaded at ```0xE8000000```

EL3_MONITOR is loaded at ```0xBFE80000```
