# Decrypted parts of the Exynos 9830 (990) bootchain

I'll start this off with a notice, do not expect these to work if sent under hubble,
the decrypted parts of the bootchain will not pass the integrity checks, this is just
for anyone who wants to do firmware analysis.

Only EPBL, EL3_MONITOR, TZSW and LDFWs are encrypted but for the sake of being able to have a look
at the other stages, i've included other binaries in the folder too.

## Loading the stages into Ghidra

ALL stages should be loaded with AARCH64 V8A LE DEFAULT. Though, load addresses differ.

FWBL1 / BL1 is loaded at ```0x02022000```

EPBL is loaded at ```0x02026000```

BL2 is loaded at ```0x15600000```

LK is loaded at ```0xE8000000```

EL3_MONITOR is loaded at ```0xBFE80000```

LDFWs differ per LDFW, refer to [my extractor](https://github.com/halal-beef/ldfw-extractor?tab=readme-ov-file#example-output) for load addresses.

## Credits and acknowledgements

- [Majaahh](https://github.com/majaahh) ```For creating a script to download as many Exynos990 firmwares as possible and downloading even more for me.```
