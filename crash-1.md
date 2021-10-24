# 5.14.14 kernel crash
# AMD Ryzen 5900X

```
-- Journal begins at Fri 2021-10-08 11:47:12 CEST, ends at Sun 2021-10-24 21:09:00 CEST. --
Oct 24 19:36:33 localhost kernel: Linux version 5.14.14-xanmod2-1-default (foo@localhost.localdomain) (gcc (SUSE Linux) 11.2.1 20210816 [revision 056e324ce46a7924b5cf10f61010cf9dd2ca10e9], GNU ld (GNU Binutils; openSUSE Tumbleweed) 2.37.20210803-1) #3 SMP Sat Oct 23 18:35:38 CEST 2021
Oct 24 19:36:33 localhost kernel: Command line: BOOT_IMAGE=/boot/vmlinuz-5.14.14-xanmod2-1-default root=UUID=b53e239d-b210-494f-986f-ccc63190e2ec splash=silent quiet mitigations=off processor.max_cstate=5 idle=nomwait nowatchdog ipv6.disable=1
Oct 24 19:36:33 localhost kernel: x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'
Oct 24 19:36:33 localhost kernel: x86/fpu: Supporting XSAVE feature 0x002: 'SSE registers'
Oct 24 19:36:33 localhost kernel: x86/fpu: Supporting XSAVE feature 0x004: 'AVX registers'
Oct 24 19:36:33 localhost kernel: x86/fpu: Supporting XSAVE feature 0x200: 'Protection Keys User registers'
Oct 24 19:36:33 localhost kernel: x86/fpu: xstate_offset[2]:  576, xstate_sizes[2]:  256
Oct 24 19:36:33 localhost kernel: x86/fpu: xstate_offset[9]:  832, xstate_sizes[9]:    8
Oct 24 19:36:33 localhost kernel: x86/fpu: Enabled xstate features 0x207, context size is 840 bytes, using 'compacted' format.
Oct 24 19:36:33 localhost kernel: signal: max sigframe size: 3376
Oct 24 19:36:33 localhost kernel: BIOS-provided physical RAM map:
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x0000000000000000-0x000000000009ffff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000000a0000-0x00000000000fffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x0000000000100000-0x0000000009d1efff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x0000000009d1f000-0x0000000009ffffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x000000000a000000-0x000000000a1fffff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x000000000a200000-0x000000000a20dfff] ACPI NVS
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x000000000a20e000-0x00000000c3278fff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000c3279000-0x00000000c3279fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000c327a000-0x00000000ca45dfff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000ca45e000-0x00000000ca811fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000ca812000-0x00000000ca981fff] ACPI data
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000ca982000-0x00000000cacecfff] ACPI NVS
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000caced000-0x00000000cb9fefff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000cb9ff000-0x00000000ccffffff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000cd000000-0x00000000cfffffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000f0000000-0x00000000f7ffffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fd100000-0x00000000fd1fffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fd300000-0x00000000fd4fffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fea00000-0x00000000fea0ffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000feb80000-0x00000000fec01fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fec10000-0x00000000fec10fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fed00000-0x00000000fed00fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fed40000-0x00000000fed44fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fed80000-0x00000000fed8ffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fedc2000-0x00000000fedcffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000fedd4000-0x00000000fedd5fff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x00000000ff000000-0x00000000ffffffff] reserved
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x0000000100000000-0x000000082f2fffff] usable
Oct 24 19:36:33 localhost kernel: BIOS-e820: [mem 0x000000082f300000-0x000000082fffffff] reserved
Oct 24 19:36:33 localhost kernel: NX (Execute Disable) protection: active
Oct 24 19:36:33 localhost kernel: e820: update [mem 0x90603018-0x90614067] usable ==> usable
Oct 24 19:36:33 localhost kernel: e820: update [mem 0x90603018-0x90614067] usable ==> usable
Oct 24 19:36:33 localhost kernel: e820: update [mem 0x905e5018-0x90602057] usable ==> usable
Oct 24 19:36:33 localhost kernel: e820: update [mem 0x905e5018-0x90602057] usable ==> usable
Oct 24 19:36:33 localhost kernel: extended physical RAM map:
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000000000000-0x000000000009ffff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000000a0000-0x00000000000fffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000000100000-0x0000000009d1efff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000009d1f000-0x0000000009ffffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x000000000a000000-0x000000000a1fffff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x000000000a200000-0x000000000a20dfff] ACPI NVS
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x000000000a20e000-0x00000000905e5017] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000905e5018-0x0000000090602057] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000090602058-0x0000000090603017] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000090603018-0x0000000090614067] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000090614068-0x00000000c3278fff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000c3279000-0x00000000c3279fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000c327a000-0x00000000ca45dfff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000ca45e000-0x00000000ca811fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000ca812000-0x00000000ca981fff] ACPI data
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000ca982000-0x00000000cacecfff] ACPI NVS
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000caced000-0x00000000cb9fefff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000cb9ff000-0x00000000ccffffff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000cd000000-0x00000000cfffffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000f0000000-0x00000000f7ffffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fd100000-0x00000000fd1fffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fd300000-0x00000000fd4fffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fea00000-0x00000000fea0ffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000feb80000-0x00000000fec01fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fec10000-0x00000000fec10fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fed00000-0x00000000fed00fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fed40000-0x00000000fed44fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fed80000-0x00000000fed8ffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fedc2000-0x00000000fedcffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000fedd4000-0x00000000fedd5fff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x00000000ff000000-0x00000000ffffffff] reserved
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x0000000100000000-0x000000082f2fffff] usable
Oct 24 19:36:33 localhost kernel: reserve setup_data: [mem 0x000000082f300000-0x000000082fffffff] reserved
Oct 24 19:36:33 localhost kernel: efi: EFI v2.70 by American Megatrends
Oct 24 19:36:33 localhost kernel: efi: ACPI=0xca981000 ACPI 2.0=0xca981014 TPMFinalLog=0xcaca0000 SMBIOS=0xcb7fa000 SMBIOS 3.0=0xcb7f9000 MEMATTR=0xc5d52018 ESRT=0xc901fe98 RNG=0xcb82eb18 TPMEventLog=0xc18e1018 
Oct 24 19:36:33 localhost kernel: efi: seeding entropy pool
Oct 24 19:36:33 localhost kernel: random: fast init done
Oct 24 19:36:33 localhost kernel: SMBIOS 3.3.0 present.
Oct 24 19:36:33 localhost kernel: DMI: System manufacturer System Product Name/ROG STRIX X570-E GAMING, BIOS 4021 08/09/2021
Oct 24 19:36:33 localhost kernel: tsc: Fast TSC calibration using PIT
Oct 24 19:36:33 localhost kernel: tsc: Detected 3700.094 MHz processor
Oct 24 19:36:33 localhost kernel: e820: update [mem 0x00000000-0x00000fff] usable ==> reserved
Oct 24 19:36:33 localhost kernel: e820: remove [mem 0x000a0000-0x000fffff] usable
Oct 24 19:36:33 localhost kernel: last_pfn = 0x82f300 max_arch_pfn = 0x400000000
Oct 24 19:36:33 localhost kernel: x86/PAT: Configuration [0-7]: WB  WC  UC- UC  WB  WP  UC- WT  
Oct 24 19:36:33 localhost kernel: e820: update [mem 0xcaa40000-0xcaa4ffff] usable ==> reserved
Oct 24 19:36:33 localhost kernel: e820: update [mem 0xd0000000-0xffffffff] usable ==> reserved
Oct 24 19:36:33 localhost kernel: last_pfn = 0xcd000 max_arch_pfn = 0x400000000
Oct 24 19:36:33 localhost kernel: esrt: Reserving ESRT space from 0x00000000c901fe98 to 0x00000000c901fed0.
Oct 24 19:36:33 localhost kernel: e820: update [mem 0xc901f000-0xc901ffff] usable ==> reserved
Oct 24 19:36:33 localhost kernel: Using GB pages for direct mapping
Oct 24 19:36:33 localhost kernel: Secure boot disabled
Oct 24 19:36:33 localhost kernel: RAMDISK: [mem 0x3b04a000-0x3ca74fff]
Oct 24 19:36:33 localhost kernel: ACPI: Early table checksum verification disabled
Oct 24 19:36:33 localhost kernel: ACPI: RSDP 0x00000000CA981014 000024 (v02 ALASKA)
Oct 24 19:36:33 localhost kernel: ACPI: XSDT 0x00000000CA980728 0000E4 (v01 ALASKA A M I    01072009 AMI  01000013)
Oct 24 19:36:33 localhost kernel: ACPI: FACP 0x00000000CA971000 000114 (v06 ALASKA A M I    01072009 AMI  00010013)
Oct 24 19:36:33 localhost kernel: ACPI: DSDT 0x00000000CA962000 00E2CD (v02 ALASKA A M I    01072009 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: FACS 0x00000000CACD0000 000040
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA977000 008C98 (v02 AMD    AmdTable 00000002 MSFT 04000000)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA973000 003B1B (v01 AMD    AMD AOD  00000001 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA972000 000164 (v02 ALASKA CPUSSDT  01072009 AMI  01072009)
Oct 24 19:36:33 localhost kernel: ACPI: FIDT 0x00000000CA961000 00009C (v01 ALASKA A M I    01072009 AMI  00010013)
Oct 24 19:36:33 localhost kernel: ACPI: FPDT 0x00000000CA85B000 000044 (v01 ALASKA A M I    01072009 AMI  01000013)
Oct 24 19:36:33 localhost kernel: ACPI: MCFG 0x00000000CA95F000 00003C (v01 ALASKA A M I    01072009 MSFT 00010013)
Oct 24 19:36:33 localhost kernel: ACPI: HPET 0x00000000CA95E000 000038 (v01 ALASKA A M I    01072009 AMI  00000005)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA95D000 000024 (v01 AMD    BIXBY    00001000 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: IVRS 0x00000000CA95B000 0000D0 (v02 AMD    AmdTable 00000001 AMD  00000001)
Oct 24 19:36:33 localhost kernel: ACPI: VFCT 0x00000000CA94C000 00EA84 (v01 ALASKA A M I    00000001 AMD  31504F47)
Oct 24 19:36:33 localhost kernel: ACPI: BGRT 0x00000000CA94B000 000038 (v01 ALASKA A M I    01072009 AMI  00010013)
Oct 24 19:36:33 localhost kernel: ACPI: WPBT 0x00000000CA871000 00003C (v01 ALASKA A M I    00000001 ASUS 00000001)
Oct 24 19:36:33 localhost kernel: ACPI: TPM2 0x00000000CA870000 00004C (v04 ALASKA A M I    00000001 AMI  00000000)
Oct 24 19:36:33 localhost kernel: ACPI: PCCT 0x00000000CA86F000 00006E (v02 AMD    AmdTable 00000001 AMD  00000001)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA869000 005EF9 (v02 AMD    AmdTable 00000001 AMD  00000001)
Oct 24 19:36:33 localhost kernel: ACPI: CRAT 0x00000000CA867000 001118 (v01 AMD    AmdTable 00000001 AMD  00000001)
Oct 24 19:36:33 localhost kernel: ACPI: CDIT 0x00000000CA866000 000029 (v01 AMD    AmdTable 00000001 AMD  00000001)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA865000 00022A (v01 AMD    QOGIRDGP 00000001 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA863000 0010AC (v01 AMD    QOGIRTPX 00000001 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA862000 00052C (v01 AMD    QOGIRNOI 00000001 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: SSDT 0x00000000CA85E000 003EAC (v01 AMD    QOGIRN   00000001 INTL 20120913)
Oct 24 19:36:33 localhost kernel: ACPI: WSMT 0x00000000CA85D000 000028 (v01 ALASKA A M I    01072009 AMI  00010013)
Oct 24 19:36:33 localhost kernel: ACPI: APIC 0x00000000CA85C000 00015E (v03 ALASKA A M I    01072009 AMI  00010013)
Oct 24 19:36:33 localhost kernel: ACPI: Reserving FACP table memory at [mem 0xca971000-0xca971113]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving DSDT table memory at [mem 0xca962000-0xca9702cc]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving FACS table memory at [mem 0xcacd0000-0xcacd003f]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca977000-0xca97fc97]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca973000-0xca976b1a]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca972000-0xca972163]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving FIDT table memory at [mem 0xca961000-0xca96109b]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving FPDT table memory at [mem 0xca85b000-0xca85b043]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving MCFG table memory at [mem 0xca95f000-0xca95f03b]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving HPET table memory at [mem 0xca95e000-0xca95e037]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca95d000-0xca95d023]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving IVRS table memory at [mem 0xca95b000-0xca95b0cf]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving VFCT table memory at [mem 0xca94c000-0xca95aa83]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving BGRT table memory at [mem 0xca94b000-0xca94b037]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving WPBT table memory at [mem 0xca871000-0xca87103b]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving TPM2 table memory at [mem 0xca870000-0xca87004b]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving PCCT table memory at [mem 0xca86f000-0xca86f06d]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca869000-0xca86eef8]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving CRAT table memory at [mem 0xca867000-0xca868117]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving CDIT table memory at [mem 0xca866000-0xca866028]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca865000-0xca865229]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca863000-0xca8640ab]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca862000-0xca86252b]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving SSDT table memory at [mem 0xca85e000-0xca861eab]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving WSMT table memory at [mem 0xca85d000-0xca85d027]
Oct 24 19:36:33 localhost kernel: ACPI: Reserving APIC table memory at [mem 0xca85c000-0xca85c15d]
Oct 24 19:36:33 localhost kernel: No NUMA configuration found
Oct 24 19:36:33 localhost kernel: Faking a node at [mem 0x0000000000000000-0x000000082f2fffff]
Oct 24 19:36:33 localhost kernel: NODE_DATA(0) allocated [mem 0x82f2d5000-0x82f2fffff]
Oct 24 19:36:33 localhost kernel: Zone ranges:
Oct 24 19:36:33 localhost kernel:   DMA      [mem 0x0000000000001000-0x0000000000ffffff]
Oct 24 19:36:33 localhost kernel:   DMA32    [mem 0x0000000001000000-0x00000000ffffffff]
Oct 24 19:36:33 localhost kernel:   Normal   [mem 0x0000000100000000-0x000000082f2fffff]
Oct 24 19:36:33 localhost kernel:   Device   empty
Oct 24 19:36:33 localhost kernel: Movable zone start for each node
Oct 24 19:36:33 localhost kernel: Early memory node ranges
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x0000000000001000-0x000000000009ffff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x0000000000100000-0x0000000009d1efff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x000000000a000000-0x000000000a1fffff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x000000000a20e000-0x00000000c3278fff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x00000000c327a000-0x00000000ca45dfff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x00000000cb9ff000-0x00000000ccffffff]
Oct 24 19:36:33 localhost kernel:   node   0: [mem 0x0000000100000000-0x000000082f2fffff]
Oct 24 19:36:33 localhost kernel: Initmem setup node 0 [mem 0x0000000000001000-0x000000082f2fffff]
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA: 1 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA: 96 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA32: 737 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA32: 14 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA32: 1 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone DMA32: 5537 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone Normal: 12288 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: On node 0, zone Normal: 3328 pages in unavailable ranges
Oct 24 19:36:33 localhost kernel: ACPI: PM-Timer IO Port: 0x808
Oct 24 19:36:33 localhost kernel: ACPI: LAPIC_NMI (acpi_id[0xff] high edge lint[0x1])
Oct 24 19:36:33 localhost kernel: IOAPIC[0]: apic_id 25, version 33, address 0xfec00000, GSI 0-23
Oct 24 19:36:33 localhost kernel: IOAPIC[1]: apic_id 26, version 33, address 0xfec01000, GSI 24-55
Oct 24 19:36:33 localhost kernel: ACPI: INT_SRC_OVR (bus 0 bus_irq 0 global_irq 2 dfl dfl)
Oct 24 19:36:33 localhost kernel: ACPI: INT_SRC_OVR (bus 0 bus_irq 9 global_irq 9 low level)
Oct 24 19:36:33 localhost kernel: ACPI: Using ACPI (MADT) for SMP configuration information
Oct 24 19:36:33 localhost kernel: ACPI: HPET id: 0x10228201 base: 0xfed00000
Oct 24 19:36:33 localhost kernel: e820: update [mem 0xc66a1000-0xc6794fff] usable ==> reserved
Oct 24 19:36:33 localhost kernel: smpboot: Allowing 32 CPUs, 8 hotplug CPUs
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x00000000-0x00000fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x000a0000-0x000fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x09d1f000-0x09ffffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x0a200000-0x0a20dfff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x905e5000-0x905e5fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x90602000-0x90602fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x90603000-0x90603fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0x90614000-0x90614fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xc3279000-0xc3279fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xc66a1000-0xc6794fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xc901f000-0xc901ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xca45e000-0xca811fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xca812000-0xca981fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xca982000-0xcacecfff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xcaced000-0xcb9fefff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xcd000000-0xcfffffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xd0000000-0xefffffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xf0000000-0xf7ffffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xf8000000-0xfd0fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfd100000-0xfd1fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfd200000-0xfd2fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfd300000-0xfd4fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfd500000-0xfe9fffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfea00000-0xfea0ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfea10000-0xfeb7ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfeb80000-0xfec01fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfec02000-0xfec0ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfec10000-0xfec10fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfec11000-0xfecfffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed00000-0xfed00fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed01000-0xfed3ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed40000-0xfed44fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed45000-0xfed7ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed80000-0xfed8ffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfed90000-0xfedc1fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfedc2000-0xfedcffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfedd0000-0xfedd3fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfedd4000-0xfedd5fff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xfedd6000-0xfeffffff]
Oct 24 19:36:33 localhost kernel: PM: hibernation: Registered nosave memory: [mem 0xff000000-0xffffffff]
Oct 24 19:36:33 localhost kernel: [mem 0xd0000000-0xefffffff] available for PCI devices
Oct 24 19:36:33 localhost kernel: Booting paravirtualized kernel on bare hardware
Oct 24 19:36:33 localhost kernel: clocksource: refined-jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 3821924579961850 ns
Oct 24 19:36:33 localhost kernel: setup_percpu: NR_CPUS:8192 nr_cpumask_bits:32 nr_cpu_ids:32 nr_node_ids:1
Oct 24 19:36:33 localhost kernel: percpu: Embedded 59 pages/cpu s204800 r8192 d28672 u262144
Oct 24 19:36:33 localhost kernel: pcpu-alloc: s204800 r8192 d28672 u262144 alloc=1*2097152
Oct 24 19:36:33 localhost kernel: pcpu-alloc: [0] 00 01 02 03 04 05 06 07 [0] 08 09 10 11 12 13 14 15 
Oct 24 19:36:33 localhost kernel: pcpu-alloc: [0] 16 17 18 19 20 21 22 23 [0] 24 25 26 27 28 29 30 31 
Oct 24 19:36:33 localhost kernel: Built 1 zonelists, mobility grouping on.  Total pages: 8235717
Oct 24 19:36:33 localhost kernel: Policy zone: Normal
Oct 24 19:36:33 localhost kernel: Kernel command line: BOOT_IMAGE=/boot/vmlinuz-5.14.14-xanmod2-1-default root=UUID=b53e239d-b210-494f-986f-ccc63190e2ec splash=silent quiet mitigations=off processor.max_cstate=5 idle=nomwait nowatchdog ipv6.disable=1
Oct 24 19:36:33 localhost kernel: Unknown command line parameters: BOOT_IMAGE=/boot/vmlinuz-5.14.14-xanmod2-1-default splash=silent
Oct 24 19:36:33 localhost kernel: printk: log_buf_len individual max cpu contribution: 32768 bytes
Oct 24 19:36:33 localhost kernel: printk: log_buf_len total cpu_extra contributions: 1015808 bytes
Oct 24 19:36:33 localhost kernel: printk: log_buf_len min size: 262144 bytes
Oct 24 19:36:33 localhost kernel: printk: log_buf_len: 2097152 bytes
Oct 24 19:36:33 localhost kernel: printk: early log buf free: 243488(92%)
Oct 24 19:36:33 localhost kernel: Dentry cache hash table entries: 4194304 (order: 13, 33554432 bytes, linear)
Oct 24 19:36:33 localhost kernel: Inode-cache hash table entries: 2097152 (order: 12, 16777216 bytes, linear)
Oct 24 19:36:33 localhost kernel: mem auto-init: stack:off, heap alloc:off, heap free:off
Oct 24 19:36:33 localhost kernel: Memory: 3313348K/33466424K available (14344K kernel code, 3234K rwdata, 8824K rodata, 2752K init, 6332K bss, 793172K reserved, 0K cma-reserved)
Oct 24 19:36:33 localhost kernel: random: get_random_u64 called from __kmem_cache_create+0x24/0x520 with crng_init=1
Oct 24 19:36:33 localhost kernel: SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=32, Nodes=1
Oct 24 19:36:33 localhost kernel: ftrace: allocating 40456 entries in 159 pages
Oct 24 19:36:33 localhost kernel: ftrace: allocated 159 pages with 6 groups
Oct 24 19:36:33 localhost kernel: rcu: Hierarchical RCU implementation.
Oct 24 19:36:33 localhost kernel: rcu:         RCU event tracing is enabled.
Oct 24 19:36:33 localhost kernel: rcu:         RCU restricting CPUs from NR_CPUS=8192 to nr_cpu_ids=32.
Oct 24 19:36:33 localhost kernel:         Rude variant of Tasks RCU enabled.
Oct 24 19:36:33 localhost kernel:         Tracing variant of Tasks RCU enabled.
Oct 24 19:36:33 localhost kernel: rcu: RCU calculated value of scheduler-enlistment delay is 50 jiffies.
Oct 24 19:36:33 localhost kernel: rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=32
Oct 24 19:36:33 localhost kernel: NR_IRQS: 524544, nr_irqs: 1224, preallocated irqs: 16
Oct 24 19:36:33 localhost kernel: random: crng done (trusting CPU's manufacturer)
Oct 24 19:36:33 localhost kernel: Console: colour dummy device 80x25
Oct 24 19:36:33 localhost kernel: printk: console [tty0] enabled
Oct 24 19:36:33 localhost kernel: ACPI: Core revision 20210604
Oct 24 19:36:33 localhost kernel: clocksource: hpet: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 133484873504 ns
Oct 24 19:36:33 localhost kernel: APIC: Switch to symmetric I/O mode setup
Oct 24 19:36:33 localhost kernel: Switched APIC routing to physical flat.
Oct 24 19:36:33 localhost kernel: ..TIMER: vector=0x30 apic1=0 pin1=2 apic2=-1 pin2=-1
Oct 24 19:36:33 localhost kernel: clocksource: tsc-early: mask: 0xffffffffffffffff max_cycles: 0x6aab5d8f64e, max_idle_ns: 881590986809 ns
Oct 24 19:36:33 localhost kernel: Calibrating delay loop (skipped), value calculated using timer frequency.. 7400.18 BogoMIPS (lpj=7400188)
Oct 24 19:36:33 localhost kernel: pid_max: default: 32768 minimum: 301
Oct 24 19:36:33 localhost kernel: LSM: Security Framework initializing
Oct 24 19:36:33 localhost kernel: AppArmor: AppArmor initialized
Oct 24 19:36:33 localhost kernel: Mount-cache hash table entries: 65536 (order: 7, 524288 bytes, linear)
Oct 24 19:36:33 localhost kernel: Mountpoint-cache hash table entries: 65536 (order: 7, 524288 bytes, linear)
Oct 24 19:36:33 localhost kernel: x86/cpu: User Mode Instruction Prevention (UMIP) activated
Oct 24 19:36:33 localhost kernel: LVT offset 1 assigned for vector 0xf9
Oct 24 19:36:33 localhost kernel: LVT offset 2 assigned for vector 0xf4
Oct 24 19:36:33 localhost kernel: Last level iTLB entries: 4KB 512, 2MB 512, 4MB 256
Oct 24 19:36:33 localhost kernel: Last level dTLB entries: 4KB 2048, 2MB 2048, 4MB 1024, 1GB 0
Oct 24 19:36:33 localhost kernel: Speculative Store Bypass: Vulnerable
Oct 24 19:36:33 localhost kernel: Freeing SMP alternatives memory: 36K
Oct 24 19:36:33 localhost kernel: smpboot: CPU0: AMD Ryzen 9 5900X 12-Core Processor (family: 0x19, model: 0x21, stepping: 0x0)
Oct 24 19:36:33 localhost kernel: Performance Events: Fam17h+ core perfctr, AMD PMU driver.
Oct 24 19:36:33 localhost kernel: ... version:                0
Oct 24 19:36:33 localhost kernel: ... bit width:              48
Oct 24 19:36:33 localhost kernel: ... generic registers:      6
Oct 24 19:36:33 localhost kernel: ... value mask:             0000ffffffffffff
Oct 24 19:36:33 localhost kernel: ... max period:             00007fffffffffff
Oct 24 19:36:33 localhost kernel: ... fixed-purpose events:   0
Oct 24 19:36:33 localhost kernel: ... event mask:             000000000000003f
Oct 24 19:36:33 localhost kernel: rcu: Hierarchical SRCU implementation.
Oct 24 19:36:33 localhost kernel: smp: Bringing up secondary CPUs ...
Oct 24 19:36:33 localhost kernel: x86: Booting SMP configuration:
Oct 24 19:36:33 localhost kernel: .... node  #0, CPUs:        #1  #2  #3  #4  #5  #6  #7  #8  #9 #10 #11 #12 #13 #14 #15 #16 #17 #18 #19 #20 #21 #22 #23
Oct 24 19:36:33 localhost kernel: smp: Brought up 1 node, 24 CPUs
Oct 24 19:36:33 localhost kernel: smpboot: Max logical packages: 2
Oct 24 19:36:33 localhost kernel: smpboot: Total of 24 processors activated (177604.51 BogoMIPS)
Oct 24 19:36:33 localhost kernel: node 0 deferred pages initialised in 20ms
Oct 24 19:36:33 localhost kernel: devtmpfs: initialized
Oct 24 19:36:33 localhost kernel: x86/mm: Memory block size: 128MB
Oct 24 19:36:33 localhost kernel: ACPI: PM: Registering ACPI NVS region [mem 0x0a200000-0x0a20dfff] (57344 bytes)
Oct 24 19:36:33 localhost kernel: ACPI: PM: Registering ACPI NVS region [mem 0xca982000-0xcacecfff] (3584000 bytes)
Oct 24 19:36:33 localhost kernel: clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 3822520892550000 ns
Oct 24 19:36:33 localhost kernel: futex hash table entries: 8192 (order: 7, 524288 bytes, linear)
Oct 24 19:36:33 localhost kernel: futex2 hash table entries: 8192 (order: 5, 196608 bytes, linear)
Oct 24 19:36:33 localhost kernel: pinctrl core: initialized pinctrl subsystem
Oct 24 19:36:33 localhost kernel: PM: RTC time: 17:36:31, date: 2021-10-24
Oct 24 19:36:33 localhost kernel: NET: Registered PF_NETLINK/PF_ROUTE protocol family
Oct 24 19:36:33 localhost kernel: DMA: preallocated 4096 KiB GFP_KERNEL pool for atomic allocations
Oct 24 19:36:33 localhost kernel: DMA: preallocated 4096 KiB GFP_KERNEL|GFP_DMA pool for atomic allocations
Oct 24 19:36:33 localhost kernel: DMA: preallocated 4096 KiB GFP_KERNEL|GFP_DMA32 pool for atomic allocations
Oct 24 19:36:33 localhost kernel: audit: initializing netlink subsys (disabled)
Oct 24 19:36:33 localhost kernel: audit: type=2000 audit(1635096991.196:1): state=initialized audit_enabled=0 res=1
Oct 24 19:36:33 localhost kernel: thermal_sys: Registered thermal governor 'fair_share'
Oct 24 19:36:33 localhost kernel: thermal_sys: Registered thermal governor 'bang_bang'
Oct 24 19:36:33 localhost kernel: thermal_sys: Registered thermal governor 'step_wise'
Oct 24 19:36:33 localhost kernel: thermal_sys: Registered thermal governor 'user_space'
Oct 24 19:36:33 localhost kernel: cpuidle: using governor ladder
Oct 24 19:36:33 localhost kernel: cpuidle: using governor menu
Oct 24 19:36:33 localhost kernel: Detected 1 PCC Subspaces
Oct 24 19:36:33 localhost kernel: Registering PCC driver as Mailbox controller
Oct 24 19:36:33 localhost kernel: ACPI: bus type PCI registered
Oct 24 19:36:33 localhost kernel: acpiphp: ACPI Hot Plug PCI Controller Driver version: 0.5
Oct 24 19:36:33 localhost kernel: PCI: MMCONFIG for domain 0000 [bus 00-7f] at [mem 0xf0000000-0xf7ffffff] (base 0xf0000000)
Oct 24 19:36:33 localhost kernel: PCI: MMCONFIG at [mem 0xf0000000-0xf7ffffff] reserved in E820
Oct 24 19:36:33 localhost kernel: PCI: Using configuration type 1 for base access
Oct 24 19:36:33 localhost kernel: Kprobes globally optimized
Oct 24 19:36:33 localhost kernel: HugeTLB registered 1.00 GiB page size, pre-allocated 0 pages
Oct 24 19:36:33 localhost kernel: HugeTLB registered 2.00 MiB page size, pre-allocated 0 pages
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Module Device)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Processor Device)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(3.0 _SCP Extensions)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Processor Aggregator Device)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Linux-Dell-Video)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Linux-Lenovo-NV-HDMI-Audio)
Oct 24 19:36:33 localhost kernel: ACPI: Added _OSI(Linux-HPI-Hybrid-Graphics)
Oct 24 19:36:33 localhost kernel: ACPI: 10 ACPI AML tables successfully acquired and loaded
Oct 24 19:36:33 localhost kernel: ACPI: [Firmware Bug]: BIOS _OSI(Linux) query ignored
Oct 24 19:36:33 localhost kernel: ACPI: EC: EC started
Oct 24 19:36:33 localhost kernel: ACPI: EC: interrupt blocked
Oct 24 19:36:33 localhost kernel: ACPI: EC: EC_CMD/EC_SC=0x66, EC_DATA=0x62
Oct 24 19:36:33 localhost kernel: ACPI: \_SB_.PCI0.SBRG.EC0_: Boot DSDT EC used to handle transactions
Oct 24 19:36:33 localhost kernel: ACPI: Interpreter enabled
Oct 24 19:36:33 localhost kernel: ACPI: PM: (supports S0 S3 S4 S5)
Oct 24 19:36:33 localhost kernel: ACPI: Using IOAPIC for interrupt routing
Oct 24 19:36:33 localhost kernel: PCI: Using host bridge windows from ACPI; if necessary, use "pci=nocrs" and report a bug
Oct 24 19:36:33 localhost kernel: ACPI: Enabled 2 GPEs in block 00 to 1F
Oct 24 19:36:33 localhost kernel: ACPI: PCI Root Bridge [PCI0] (domain 0000 [bus 00-ff])
Oct 24 19:36:33 localhost kernel: acpi PNP0A08:00: _OSC: OS supports [ExtendedConfig ASPM ClockPM Segments MSI EDR HPX-Type3]
Oct 24 19:36:33 localhost kernel: acpi PNP0A08:00: _OSC: platform does not support [PCIeHotplug SHPCHotplug PME LTR DPC]
Oct 24 19:36:33 localhost kernel: acpi PNP0A08:00: _OSC: OS now controls [AER PCIeCapability]
Oct 24 19:36:33 localhost kernel: acpi PNP0A08:00: [Firmware Info]: MMCONFIG for domain 0000 [bus 00-7f] only partially covers this bridge
Oct 24 19:36:33 localhost kernel: PCI host bridge to bus 0000:00
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [io  0x0000-0x03af window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [io  0x03e0-0x0cf7 window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [io  0x03b0-0x03df window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [io  0x0d00-0xffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [mem 0x000a0000-0x000bffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [mem 0x000c0000-0x000dffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [mem 0xd0000000-0xfec02fff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [mem 0xfee00000-0xffffffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: root bus resource [bus 00-ff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:00.0: [1022:1480] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:00.2: [1022:1481] type 00 class 0x080600
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: [1022:1483] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: [1022:1483] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:02.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1: [1022:1483] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:04.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:05.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: [1022:1484] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.0: [1022:1482] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: [1022:1484] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:14.0: [1022:790b] type 00 class 0x0c0500
Oct 24 19:36:33 localhost kernel: pci 0000:00:14.3: [1022:790e] type 00 class 0x060100
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.0: [1022:1440] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.1: [1022:1441] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.2: [1022:1442] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.3: [1022:1443] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.4: [1022:1444] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.5: [1022:1445] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.6: [1022:1446] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.7: [1022:1447] type 00 class 0x060000
Oct 24 19:36:33 localhost kernel: pci 0000:01:00.0: [144d:a808] type 00 class 0x010802
Oct 24 19:36:33 localhost kernel: pci 0000:01:00.0: reg 0x10: [mem 0xfcf00000-0xfcf03fff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: PCI bridge to [bus 01]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1:   bridge window [mem 0xfcf00000-0xfcffffff]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: [1022:57ad] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: 63.012 Gb/s available PCIe bandwidth, limited by 16.0 GT/s PCIe x4 link at 0000:00:01.2 (capable of 126.024 Gb/s with 16.0 GT/s PCIe x8 link)
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: PCI bridge to [bus 02-08]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2:   bridge window [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: [1022:57a3] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: [1022:57a3] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: [1022:57a4] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: [1022:57a4] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: [1022:57a4] type 01 class 0x060400
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: PCI bridge to [bus 03-08]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0:   bridge window [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:04:00.0: [144d:a808] type 00 class 0x010802
Oct 24 19:36:33 localhost kernel: pci 0000:04:00.0: reg 0x10: [mem 0xfca00000-0xfca03fff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: PCI bridge to [bus 04]
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0:   bridge window [mem 0xfca00000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: [8086:1539] type 00 class 0x020000
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: reg 0x10: [mem 0xfc900000-0xfc91ffff]
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: reg 0x18: [io  0xf000-0xf01f]
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: reg 0x1c: [mem 0xfc920000-0xfc923fff]
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: PCI bridge to [bus 05]
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0:   bridge window [mem 0xfc900000-0xfc9fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.0: [1022:1485] type 00 class 0x130000
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.0: 63.012 Gb/s available PCIe bandwidth, limited by 16.0 GT/s PCIe x4 link at 0000:00:01.2 (capable of 252.048 Gb/s with 16.0 GT/s PCIe x16 link)
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.1: [1022:149c] type 00 class 0x0c0330
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.1: reg 0x10: [mem 0xfc600000-0xfc6fffff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.1: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.1: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.3: [1022:149c] type 00 class 0x0c0330
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.3: reg 0x10: [mem 0xfc500000-0xfc5fffff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.3: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.3: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: PCI bridge to [bus 06]
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0:   bridge window [mem 0xfc500000-0xfc6fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: [1022:7901] type 00 class 0x010601
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: reg 0x24: [mem 0xfc800000-0xfc8007ff]
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: PME# supported from D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: 63.012 Gb/s available PCIe bandwidth, limited by 16.0 GT/s PCIe x4 link at 0000:00:01.2 (capable of 252.048 Gb/s with 16.0 GT/s PCIe x16 link)
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: PCI bridge to [bus 07]
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0:   bridge window [mem 0xfc800000-0xfc8fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: [1022:7901] type 00 class 0x010601
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: reg 0x24: [mem 0xfc700000-0xfc7007ff]
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: PME# supported from D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: 63.012 Gb/s available PCIe bandwidth, limited by 16.0 GT/s PCIe x4 link at 0000:00:01.2 (capable of 252.048 Gb/s with 16.0 GT/s PCIe x16 link)
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: PCI bridge to [bus 08]
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0:   bridge window [mem 0xfc700000-0xfc7fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: [1002:67df] type 00 class 0x030000
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: reg 0x10: [mem 0xd0000000-0xdfffffff 64bit pref]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: reg 0x18: [mem 0xe0000000-0xe01fffff 64bit pref]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: reg 0x20: [io  0xe000-0xe0ff]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: reg 0x24: [mem 0xfce00000-0xfce3ffff]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: reg 0x30: [mem 0xfce40000-0xfce5ffff pref]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: BAR 0: assigned to efifb
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: supports D1 D2
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: PME# supported from D1 D2 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.1: [1002:aaf0] type 00 class 0x040300
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.1: reg 0x10: [mem 0xfce60000-0xfce63fff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.1: supports D1 D2
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1: PCI bridge to [bus 09]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [io  0xe000-0xefff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [mem 0xfce00000-0xfcefffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [mem 0xd0000000-0xe01fffff 64bit pref]
Oct 24 19:36:33 localhost kernel: pci 0000:0a:00.0: [1022:148a] type 00 class 0x130000
Oct 24 19:36:33 localhost kernel: pci 0000:0a:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: PCI bridge to [bus 0a]
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.0: [1022:1485] type 00 class 0x130000
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.0: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.1: [1022:1486] type 00 class 0x108000
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.1: reg 0x18: [mem 0xfcc00000-0xfccfffff]
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.1: reg 0x24: [mem 0xfcd00000-0xfcd01fff]
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.1: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.3: [1022:149c] type 00 class 0x0c0330
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.3: reg 0x10: [mem 0xfcb00000-0xfcbfffff 64bit]
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.3: enabling Extended Tags
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.3: PME# supported from D0 D3hot D3cold
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: PCI bridge to [bus 0b]
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1:   bridge window [mem 0xfcb00000-0xfcdfffff]
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKA configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKB configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKC configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKD configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKE configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKF configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKG configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: PCI: Interrupt link LNKH configured for IRQ 0
Oct 24 19:36:33 localhost kernel: ACPI: EC: interrupt unblocked
Oct 24 19:36:33 localhost kernel: ACPI: EC: event unblocked
Oct 24 19:36:33 localhost kernel: ACPI: EC: EC_CMD/EC_SC=0x66, EC_DATA=0x62
Oct 24 19:36:33 localhost kernel: ACPI: EC: GPE=0x2
Oct 24 19:36:33 localhost kernel: ACPI: \_SB_.PCI0.SBRG.EC0_: Boot DSDT EC initialization complete
Oct 24 19:36:33 localhost kernel: ACPI: \_SB_.PCI0.SBRG.EC0_: EC: Used to handle transactions and events
Oct 24 19:36:33 localhost kernel: iommu: Default domain type: Passthrough 
Oct 24 19:36:33 localhost kernel: SCSI subsystem initialized
Oct 24 19:36:33 localhost kernel: libata version 3.00 loaded.
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: vgaarb: VGA device added: decodes=io+mem,owns=none,locks=none
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: vgaarb: bridge control possible
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: vgaarb: setting as boot device
Oct 24 19:36:33 localhost kernel: vgaarb: loaded
Oct 24 19:36:33 localhost kernel: pps_core: LinuxPPS API ver. 1 registered
Oct 24 19:36:33 localhost kernel: pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
Oct 24 19:36:33 localhost kernel: PTP clock support registered
Oct 24 19:36:33 localhost kernel: EDAC MC: Ver: 3.0.0
Oct 24 19:36:33 localhost kernel: Registered efivars operations
Oct 24 19:36:33 localhost kernel: NetLabel: Initializing
Oct 24 19:36:33 localhost kernel: NetLabel:  domain hash size = 128
Oct 24 19:36:33 localhost kernel: NetLabel:  protocols = UNLABELED CIPSOv4 CALIPSO
Oct 24 19:36:33 localhost kernel: NetLabel:  unlabeled traffic allowed by default
Oct 24 19:36:33 localhost kernel: PCI: Using ACPI for IRQ routing
Oct 24 19:36:33 localhost kernel: PCI: pci_cache_line_size set to 64 bytes
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0x09d1f000-0x0bffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0x0a200000-0x0bffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0x905e5018-0x93ffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0x90603018-0x93ffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0xc3279000-0xc3ffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0xc66a1000-0xc7ffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0xc901f000-0xcbffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0xca45e000-0xcbffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0xcd000000-0xcfffffff]
Oct 24 19:36:33 localhost kernel: e820: reserve RAM buffer [mem 0x82f300000-0x82fffffff]
Oct 24 19:36:33 localhost kernel: hpet0: at MMIO 0xfed00000, IRQs 2, 8, 0
Oct 24 19:36:33 localhost kernel: hpet0: 3 comparators, 32-bit 14.318180 MHz counter
Oct 24 19:36:33 localhost kernel: clocksource: Switched to clocksource tsc-early
Oct 24 19:36:33 localhost kernel: VFS: Disk quotas dquot_6.6.0
Oct 24 19:36:33 localhost kernel: VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
Oct 24 19:36:33 localhost kernel: AppArmor: AppArmor Filesystem Enabled
Oct 24 19:36:33 localhost kernel: pnp: PnP ACPI init
Oct 24 19:36:33 localhost kernel: system 00:00: [mem 0xf0000000-0xf7ffffff] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:01: [mem 0xfd100000-0xfd1fffff] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:03: [io  0x0290-0x029f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:03: [io  0x0200-0x021f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x04d0-0x04d1] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x040b] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x04d6] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c00-0x0c01] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c14] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c50-0x0c51] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c52] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c6c] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0c6f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0cd8-0x0cdf] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0800-0x089f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0b00-0x0b0f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0b20-0x0b3f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0900-0x090f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [io  0x0910-0x091f] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfec00000-0xfec00fff] could not be reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfec01000-0xfec01fff] could not be reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfedc0000-0xfedc0fff] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfee00000-0xfee00fff] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfed80000-0xfed8ffff] could not be reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xfec10000-0xfec10fff] has been reserved
Oct 24 19:36:33 localhost kernel: system 00:04: [mem 0xff000000-0xffffffff] has been reserved
Oct 24 19:36:33 localhost kernel: pnp: PnP ACPI: found 5 devices
Oct 24 19:36:33 localhost kernel: clocksource: acpi_pm: mask: 0xffffff max_cycles: 0xffffff, max_idle_ns: 2085701024 ns
Oct 24 19:36:33 localhost kernel: NET: Registered PF_INET protocol family
Oct 24 19:36:33 localhost kernel: IP idents hash table entries: 262144 (order: 9, 2097152 bytes, linear)
Oct 24 19:36:33 localhost kernel: tcp_listen_portaddr_hash hash table entries: 16384 (order: 6, 262144 bytes, linear)
Oct 24 19:36:33 localhost kernel: TCP established hash table entries: 262144 (order: 9, 2097152 bytes, linear)
Oct 24 19:36:33 localhost kernel: TCP bind hash table entries: 65536 (order: 8, 1048576 bytes, linear)
Oct 24 19:36:33 localhost kernel: TCP: Hash tables configured (established 262144 bind 65536)
Oct 24 19:36:33 localhost kernel: MPTCP token hash table entries: 32768 (order: 7, 786432 bytes, linear)
Oct 24 19:36:33 localhost kernel: UDP hash table entries: 16384 (order: 7, 524288 bytes, linear)
Oct 24 19:36:33 localhost kernel: UDP-Lite hash table entries: 16384 (order: 7, 524288 bytes, linear)
Oct 24 19:36:33 localhost kernel: NET: Registered PF_UNIX/PF_LOCAL protocol family
Oct 24 19:36:33 localhost kernel: NET: Registered PF_XDP protocol family
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: PCI bridge to [bus 01]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1:   bridge window [mem 0xfcf00000-0xfcffffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: PCI bridge to [bus 04]
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0:   bridge window [mem 0xfca00000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: PCI bridge to [bus 05]
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0:   bridge window [mem 0xfc900000-0xfc9fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: PCI bridge to [bus 06]
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0:   bridge window [mem 0xfc500000-0xfc6fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: PCI bridge to [bus 07]
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0:   bridge window [mem 0xfc800000-0xfc8fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: PCI bridge to [bus 08]
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0:   bridge window [mem 0xfc700000-0xfc7fffff]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: PCI bridge to [bus 03-08]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0:   bridge window [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: PCI bridge to [bus 02-08]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2:   bridge window [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2:   bridge window [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1: PCI bridge to [bus 09]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [io  0xe000-0xefff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [mem 0xfce00000-0xfcefffff]
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1:   bridge window [mem 0xd0000000-0xe01fffff 64bit pref]
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: PCI bridge to [bus 0a]
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: PCI bridge to [bus 0b]
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1:   bridge window [mem 0xfcb00000-0xfcdfffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 4 [io  0x0000-0x03af window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 5 [io  0x03e0-0x0cf7 window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 6 [io  0x03b0-0x03df window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 7 [io  0x0d00-0xffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 8 [mem 0x000a0000-0x000bffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 9 [mem 0x000c0000-0x000dffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 10 [mem 0xd0000000-0xfec02fff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:00: resource 11 [mem 0xfee00000-0xffffffff window]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:01: resource 1 [mem 0xfcf00000-0xfcffffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:02: resource 0 [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:02: resource 1 [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:03: resource 0 [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:03: resource 1 [mem 0xfc500000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:04: resource 1 [mem 0xfca00000-0xfcafffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:05: resource 0 [io  0xf000-0xffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:05: resource 1 [mem 0xfc900000-0xfc9fffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:06: resource 1 [mem 0xfc500000-0xfc6fffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:07: resource 1 [mem 0xfc800000-0xfc8fffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:08: resource 1 [mem 0xfc700000-0xfc7fffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:09: resource 0 [io  0xe000-0xefff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:09: resource 1 [mem 0xfce00000-0xfcefffff]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:09: resource 2 [mem 0xd0000000-0xe01fffff 64bit pref]
Oct 24 19:36:33 localhost kernel: pci_bus 0000:0b: resource 1 [mem 0xfcb00000-0xfcdfffff]
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.1: D0 power state depends on 0000:09:00.0
Oct 24 19:36:33 localhost kernel: PCI: CLS 64 bytes, default 64
Oct 24 19:36:33 localhost kernel: pci 0000:00:00.2: AMD-Vi: IOMMU performance counters supported
Oct 24 19:36:33 localhost kernel: AMD-Vi: Lazy IO/TLB flushing enabled
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.0: Adding to iommu group 0
Oct 24 19:36:33 localhost kernel: Unpacking initramfs...
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.1: Adding to iommu group 1
Oct 24 19:36:33 localhost kernel: pci 0000:00:01.2: Adding to iommu group 2
Oct 24 19:36:33 localhost kernel: pci 0000:00:02.0: Adding to iommu group 3
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.0: Adding to iommu group 4
Oct 24 19:36:33 localhost kernel: pci 0000:00:03.1: Adding to iommu group 5
Oct 24 19:36:33 localhost kernel: pci 0000:00:04.0: Adding to iommu group 6
Oct 24 19:36:33 localhost kernel: pci 0000:00:05.0: Adding to iommu group 7
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.0: Adding to iommu group 8
Oct 24 19:36:33 localhost kernel: pci 0000:00:07.1: Adding to iommu group 9
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.0: Adding to iommu group 10
Oct 24 19:36:33 localhost kernel: pci 0000:00:08.1: Adding to iommu group 11
Oct 24 19:36:33 localhost kernel: pci 0000:00:14.0: Adding to iommu group 12
Oct 24 19:36:33 localhost kernel: pci 0000:00:14.3: Adding to iommu group 12
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.0: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.1: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.2: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.3: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.4: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.5: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.6: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:00:18.7: Adding to iommu group 13
Oct 24 19:36:33 localhost kernel: pci 0000:01:00.0: Adding to iommu group 14
Oct 24 19:36:33 localhost kernel: pci 0000:02:00.0: Adding to iommu group 15
Oct 24 19:36:33 localhost kernel: pci 0000:03:01.0: Adding to iommu group 16
Oct 24 19:36:33 localhost kernel: pci 0000:03:05.0: Adding to iommu group 17
Oct 24 19:36:33 localhost kernel: pci 0000:03:08.0: Adding to iommu group 18
Oct 24 19:36:33 localhost kernel: pci 0000:03:09.0: Adding to iommu group 19
Oct 24 19:36:33 localhost kernel: pci 0000:03:0a.0: Adding to iommu group 20
Oct 24 19:36:33 localhost kernel: pci 0000:04:00.0: Adding to iommu group 21
Oct 24 19:36:33 localhost kernel: pci 0000:05:00.0: Adding to iommu group 22
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.0: Adding to iommu group 18
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.1: Adding to iommu group 18
Oct 24 19:36:33 localhost kernel: pci 0000:06:00.3: Adding to iommu group 18
Oct 24 19:36:33 localhost kernel: pci 0000:07:00.0: Adding to iommu group 19
Oct 24 19:36:33 localhost kernel: pci 0000:08:00.0: Adding to iommu group 20
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.0: Adding to iommu group 23
Oct 24 19:36:33 localhost kernel: pci 0000:09:00.1: Adding to iommu group 23
Oct 24 19:36:33 localhost kernel: pci 0000:0a:00.0: Adding to iommu group 24
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.0: Adding to iommu group 25
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.1: Adding to iommu group 26
Oct 24 19:36:33 localhost kernel: pci 0000:0b:00.3: Adding to iommu group 27
Oct 24 19:36:33 localhost kernel: pci 0000:00:00.2: AMD-Vi: Found IOMMU cap 0x40
Oct 24 19:36:33 localhost kernel: AMD-Vi: Extended features (0x58f77ef22294a5a): PPR NX GT IA PC GA_vAPIC
Oct 24 19:36:33 localhost kernel: AMD-Vi: Interrupt remapping enabled
Oct 24 19:36:33 localhost kernel: PCI-DMA: Using software bounce buffering for IO (SWIOTLB)
Oct 24 19:36:33 localhost kernel: software IO TLB: mapped [mem 0x00000000bd8e1000-0x00000000c18e1000] (64MB)
Oct 24 19:36:33 localhost kernel: RAPL PMU: API unit is 2^-32 Joules, 1 fixed counters, 163840 ms ovfl timer
Oct 24 19:36:33 localhost kernel: RAPL PMU: hw unit of domain package 2^-16 Joules
Oct 24 19:36:33 localhost kernel: amd_uncore: 4  amd_df counters detected
Oct 24 19:36:33 localhost kernel: amd_uncore: 6  amd_l3 counters detected
Oct 24 19:36:33 localhost kernel: LVT offset 0 assigned for vector 0x400
Oct 24 19:36:33 localhost kernel: perf: AMD IBS detected (0x000003ff)
Oct 24 19:36:33 localhost kernel: perf/amd_iommu: Detected AMD IOMMU #0 (2 banks, 4 counters/bank).
Oct 24 19:36:33 localhost kernel: Initialise system trusted keyrings
Oct 24 19:36:33 localhost kernel: Key type blacklist registered
Oct 24 19:36:33 localhost kernel: workingset: timestamp_bits=36 max_order=23 bucket_order=0
Oct 24 19:36:33 localhost kernel: zbud: loaded
Oct 24 19:36:33 localhost kernel: integrity: Platform Keyring initialized
Oct 24 19:36:33 localhost kernel: Key type asymmetric registered
Oct 24 19:36:33 localhost kernel: Asymmetric key parser 'x509' registered
Oct 24 19:36:33 localhost kernel: Block layer SCSI generic (bsg) driver version 0.4 loaded (major 247)
Oct 24 19:36:33 localhost kernel: io scheduler mq-deadline registered
Oct 24 19:36:33 localhost kernel: io scheduler kyber registered
Oct 24 19:36:33 localhost kernel: io scheduler bfq registered
Oct 24 19:36:33 localhost kernel: pcieport 0000:00:01.1: AER: enabled with IRQ 27
Oct 24 19:36:33 localhost kernel: pcieport 0000:00:01.2: AER: enabled with IRQ 28
Oct 24 19:36:33 localhost kernel: pcieport 0000:00:03.1: AER: enabled with IRQ 29
Oct 24 19:36:33 localhost kernel: pcieport 0000:00:07.1: AER: enabled with IRQ 31
Oct 24 19:36:33 localhost kernel: pcieport 0000:00:08.1: AER: enabled with IRQ 32
Oct 24 19:36:33 localhost kernel: shpchp: Standard Hot Plug PCI Controller Driver version: 0.4
Oct 24 19:36:33 localhost kernel: efifb: probing for efifb
Oct 24 19:36:33 localhost kernel: efifb: framebuffer at 0xd0000000, using 3072k, total 3072k
Oct 24 19:36:33 localhost kernel: efifb: mode is 1024x768x32, linelength=4096, pages=1
Oct 24 19:36:33 localhost kernel: efifb: scrolling: redraw
Oct 24 19:36:33 localhost kernel: efifb: Truecolor: size=8:8:8:8, shift=24:16:8:0
Oct 24 19:36:33 localhost kernel: Console: switching to colour frame buffer device 128x48
Oct 24 19:36:33 localhost kernel: fb0: EFI VGA frame buffer device
Oct 24 19:36:33 localhost kernel: smpboot: Estimated ratio of average max frequency by base frequency (times 1024): 1197
Oct 24 19:36:33 localhost kernel: Monitor-Mwait will be used to enter C-1 state
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C000: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C002: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C004: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C006: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C008: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00A: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00C: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00E: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C010: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C012: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C014: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C016: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C001: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C003: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C005: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C007: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C009: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00B: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00D: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C00F: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C011: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C013: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C015: Found 2 idle states
Oct 24 19:36:33 localhost kernel: ACPI: \_PR_.C017: Found 2 idle states
Oct 24 19:36:33 localhost kernel: Serial: 8250/16550 driver, 32 ports, IRQ sharing enabled
Oct 24 19:36:33 localhost kernel: serial8250: ttyS0 at I/O 0x3f8 (irq = 4, base_baud = 115200) is a 16550A
Oct 24 19:36:33 localhost kernel: Non-volatile memory driver v1.3
Oct 24 19:36:33 localhost kernel: Linux agpgart interface v0.103
Oct 24 19:36:33 localhost kernel: ahci 0000:07:00.0: version 3.0
Oct 24 19:36:33 localhost kernel: ahci 0000:07:00.0: AHCI 0001.0301 32 slots 1 ports 6 Gbps 0x1 impl SATA mode
Oct 24 19:36:33 localhost kernel: ahci 0000:07:00.0: flags: 64bit ncq sntf ilck pm led clo only pmp fbs pio slum part 
Oct 24 19:36:33 localhost kernel: scsi host0: ahci
Oct 24 19:36:33 localhost kernel: ata1: SATA max UDMA/133 abar m2048@0xfc800000 port 0xfc800100 irq 40
Oct 24 19:36:33 localhost kernel: ahci 0000:08:00.0: AHCI 0001.0301 32 slots 2 ports 6 Gbps 0x22 impl SATA mode
Oct 24 19:36:33 localhost kernel: ahci 0000:08:00.0: flags: 64bit ncq sntf ilck pm led clo only pmp fbs pio slum part 
Oct 24 19:36:33 localhost kernel: scsi host1: ahci
Oct 24 19:36:33 localhost kernel: scsi host2: ahci
Oct 24 19:36:33 localhost kernel: scsi host3: ahci
Oct 24 19:36:33 localhost kernel: scsi host4: ahci
Oct 24 19:36:33 localhost kernel: scsi host5: ahci
Oct 24 19:36:33 localhost kernel: scsi host6: ahci
Oct 24 19:36:33 localhost kernel: ata2: DUMMY
Oct 24 19:36:33 localhost kernel: ata3: SATA max UDMA/133 abar m2048@0xfc700000 port 0xfc700180 irq 42
Oct 24 19:36:33 localhost kernel: ata4: DUMMY
Oct 24 19:36:33 localhost kernel: ata5: DUMMY
Oct 24 19:36:33 localhost kernel: ata6: DUMMY
Oct 24 19:36:33 localhost kernel: ata7: SATA max UDMA/133 abar m2048@0xfc700000 port 0xfc700380 irq 46
Oct 24 19:36:33 localhost kernel: i8042: PNP: No PS/2 controller found.
Oct 24 19:36:33 localhost kernel: mousedev: PS/2 mouse device common for all mice
Oct 24 19:36:33 localhost kernel: rtc_cmos 00:02: RTC can wake from S4
Oct 24 19:36:33 localhost kernel: rtc_cmos 00:02: registered as rtc0
Oct 24 19:36:33 localhost kernel: rtc_cmos 00:02: setting system clock to 2021-10-24T17:36:32 UTC (1635096992)
Oct 24 19:36:33 localhost kernel: rtc_cmos 00:02: alarms up to one month, y3k, 114 bytes nvram, hpet irqs
Oct 24 19:36:33 localhost kernel: ledtrig-cpu: registered to indicate activity on CPUs
Oct 24 19:36:33 localhost kernel: EFI Variables Facility v0.08 2004-May-17
Oct 24 19:36:33 localhost kernel: hid: raw HID events driver (C) Jiri Kosina
Oct 24 19:36:33 localhost kernel: drop_monitor: Initializing network drop monitor service
Oct 24 19:36:33 localhost kernel: IPv6: Loaded, but administratively disabled, reboot required to enable
Oct 24 19:36:33 localhost kernel: microcode: CPU0: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU1: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU2: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU3: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU4: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU5: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU6: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU7: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU8: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU9: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU10: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU11: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU12: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU13: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU14: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU15: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU16: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU17: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU18: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU19: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU20: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU21: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU22: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: CPU23: patch_level=0x0a201016
Oct 24 19:36:33 localhost kernel: microcode: Microcode Update Driver: v2.2.
Oct 24 19:36:33 localhost kernel: resctrl: L3 allocation detected
Oct 24 19:36:33 localhost kernel: resctrl: L3DATA allocation detected
Oct 24 19:36:33 localhost kernel: resctrl: L3CODE allocation detected
Oct 24 19:36:33 localhost kernel: resctrl: MB allocation detected
Oct 24 19:36:33 localhost kernel: resctrl: L3 monitoring detected
Oct 24 19:36:33 localhost kernel: IPI shorthand broadcast: enabled
Oct 24 19:36:33 localhost kernel: sched_clock: Marking stable (401651627, 314237172)->(808083340, -92194541)
Oct 24 19:36:33 localhost kernel: registered taskstats version 1
Oct 24 19:36:33 localhost kernel: Loading compiled-in X.509 certificates
Oct 24 19:36:33 localhost kernel: Loaded X.509 cert 'Build time autogenerated kernel key: ce2c6963a4813b38c0ffbf01e406c608faec682a'
Oct 24 19:36:33 localhost kernel: zswap: loaded using pool lzo/zbud
Oct 24 19:36:33 localhost kernel: page_owner is disabled
Oct 24 19:36:33 localhost kernel: Key type ._fscrypt registered
Oct 24 19:36:33 localhost kernel: Key type .fscrypt registered
Oct 24 19:36:33 localhost kernel: Key type fscrypt-provisioning registered
Oct 24 19:36:33 localhost kernel: ata1: SATA link up 6.0 Gbps (SStatus 133 SControl 300)
Oct 24 19:36:33 localhost kernel: ata7: SATA link up 6.0 Gbps (SStatus 133 SControl 300)
Oct 24 19:36:33 localhost kernel: ata7.00: supports DRM functions and may not be fully accessible
Oct 24 19:36:33 localhost kernel: ata3: SATA link up 6.0 Gbps (SStatus 133 SControl 300)
Oct 24 19:36:33 localhost kernel: ata3.00: supports DRM functions and may not be fully accessible
Oct 24 19:36:33 localhost kernel: ata7.00: disabling queued TRIM support
Oct 24 19:36:33 localhost kernel: ata7.00: ATA-11: Samsung SSD 860 EVO 500GB, RVT04B6Q, max UDMA/133
Oct 24 19:36:33 localhost kernel: ata7.00: 976773168 sectors, multi 1: LBA48 NCQ (depth 32), AA
Oct 24 19:36:33 localhost kernel: ata3.00: disabling queued TRIM support
Oct 24 19:36:33 localhost kernel: ata3.00: ATA-11: Samsung SSD 860 EVO 500GB, RVT04B6Q, max UDMA/133
Oct 24 19:36:33 localhost kernel: ata3.00: 976773168 sectors, multi 1: LBA48 NCQ (depth 32), AA
Oct 24 19:36:33 localhost kernel: ata7.00: supports DRM functions and may not be fully accessible
Oct 24 19:36:33 localhost kernel: ata3.00: supports DRM functions and may not be fully accessible
Oct 24 19:36:33 localhost kernel: ata7.00: disabling queued TRIM support
Oct 24 19:36:33 localhost kernel: ata3.00: disabling queued TRIM support
Oct 24 19:36:33 localhost kernel: ata7.00: configured for UDMA/133
Oct 24 19:36:33 localhost kernel: ata3.00: configured for UDMA/133
Oct 24 19:36:33 localhost kernel: ata1.00: ATA-10: ST4000VN008-2DR166, SC60, max UDMA/133
Oct 24 19:36:33 localhost kernel: ata1.00: 7814037168 sectors, multi 16: LBA48 NCQ (depth 32), AA
Oct 24 19:36:33 localhost kernel: ata1.00: configured for UDMA/133
Oct 24 19:36:33 localhost kernel: scsi 0:0:0:0: Direct-Access     ATA      ST4000VN008-2DR1 SC60 PQ: 0 ANSI: 5
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] 7814037168 512-byte logical blocks: (4.00 TB/3.64 TiB)
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] 4096-byte physical blocks
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] Write Protect is off
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] Mode Sense: 00 3a 00 00
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
Oct 24 19:36:33 localhost kernel: scsi 2:0:0:0: Direct-Access     ATA      Samsung SSD 860  4B6Q PQ: 0 ANSI: 5
Oct 24 19:36:33 localhost kernel: ata3.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] 976773168 512-byte logical blocks: (500 GB/466 GiB)
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] Write Protect is off
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] Mode Sense: 00 3a 00 00
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
Oct 24 19:36:33 localhost kernel: scsi 6:0:0:0: Direct-Access     ATA      Samsung SSD 860  4B6Q PQ: 0 ANSI: 5
Oct 24 19:36:33 localhost kernel: ata7.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel: ata3.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] 976773168 512-byte logical blocks: (500 GB/466 GiB)
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] Write Protect is off
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] Mode Sense: 00 3a 00 00
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
Oct 24 19:36:33 localhost kernel: ata7.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel:  sdb:
Oct 24 19:36:33 localhost kernel: ata3.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel:  sdc: sdc1 sdc2 sdc3
Oct 24 19:36:33 localhost kernel: ata7.00: Enabling discard_zeroes_data
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] supports TCG Opal
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: [sdb] Attached SCSI disk
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] supports TCG Opal
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: [sdc] Attached SCSI disk
Oct 24 19:36:33 localhost kernel:  sda: sda1
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: [sda] Attached SCSI disk
Oct 24 19:36:33 localhost kernel: Freeing initrd memory: 26796K
Oct 24 19:36:33 localhost kernel: Key type encrypted registered
Oct 24 19:36:33 localhost kernel: AppArmor: AppArmor sha1 policy hashing enabled
Oct 24 19:36:33 localhost kernel: integrity: Loading X.509 certificate: UEFI:db
Oct 24 19:36:33 localhost kernel: integrity: Loaded X.509 cert 'ASUSTeK MotherBoard SW Key Certificate: da83b990422ebc8c441f8d8b039a65a2'
Oct 24 19:36:33 localhost kernel: integrity: Loading X.509 certificate: UEFI:db
Oct 24 19:36:33 localhost kernel: integrity: Loaded X.509 cert 'ASUSTeK Notebook SW Key Certificate: b8e581e4df77a5bb4282d5ccfc00c071'
Oct 24 19:36:33 localhost kernel: integrity: Loading X.509 certificate: UEFI:db
Oct 24 19:36:33 localhost kernel: integrity: Loaded X.509 cert 'Microsoft Corporation UEFI CA 2011: 13adbf4309bd82709c8cd54f316ed522988a1bd4'
Oct 24 19:36:33 localhost kernel: integrity: Loading X.509 certificate: UEFI:db
Oct 24 19:36:33 localhost kernel: integrity: Loaded X.509 cert 'Microsoft Windows Production PCA 2011: a92902398e16c49778cd90f99e4f9ae17c55af53'
Oct 24 19:36:33 localhost kernel: integrity: Loading X.509 certificate: UEFI:db
Oct 24 19:36:33 localhost kernel: integrity: Loaded X.509 cert 'Canonical Ltd. Master Certificate Authority: ad91990bc22ab1f517048c23b6655a268e345a63'
Oct 24 19:36:33 localhost kernel: Loading compiled-in module X.509 certificates
Oct 24 19:36:33 localhost kernel: Loaded X.509 cert 'Build time autogenerated kernel key: ce2c6963a4813b38c0ffbf01e406c608faec682a'
Oct 24 19:36:33 localhost kernel: ima: Allocated hash algorithm: sha256
Oct 24 19:36:33 localhost kernel: ima: No architecture policies found
Oct 24 19:36:33 localhost kernel: evm: Initialising EVM extended attributes:
Oct 24 19:36:33 localhost kernel: evm: security.selinux
Oct 24 19:36:33 localhost kernel: evm: security.SMACK64 (disabled)
Oct 24 19:36:33 localhost kernel: evm: security.SMACK64EXEC (disabled)
Oct 24 19:36:33 localhost kernel: evm: security.SMACK64TRANSMUTE (disabled)
Oct 24 19:36:33 localhost kernel: evm: security.SMACK64MMAP (disabled)
Oct 24 19:36:33 localhost kernel: evm: security.apparmor
Oct 24 19:36:33 localhost kernel: evm: security.ima
Oct 24 19:36:33 localhost kernel: evm: security.capability
Oct 24 19:36:33 localhost kernel: evm: HMAC attrs: 0x1
Oct 24 19:36:33 localhost kernel: PM:   Magic number: 9:214:644
Oct 24 19:36:33 localhost kernel: RAS: Correctable Errors collector initialized.
Oct 24 19:36:33 localhost kernel: Freeing unused decrypted memory: 2036K
Oct 24 19:36:33 localhost kernel: Freeing unused kernel image (initmem) memory: 2752K
Oct 24 19:36:33 localhost kernel: Write protecting the kernel read-only data: 26624k
Oct 24 19:36:33 localhost kernel: Freeing unused kernel image (text/rodata gap) memory: 2036K
Oct 24 19:36:33 localhost kernel: Freeing unused kernel image (rodata/data gap) memory: 1416K
Oct 24 19:36:33 localhost kernel: Run /init as init process
Oct 24 19:36:33 localhost kernel:   with arguments:
Oct 24 19:36:33 localhost kernel:     /init
Oct 24 19:36:33 localhost kernel:   with environment:
Oct 24 19:36:33 localhost kernel:     HOME=/
Oct 24 19:36:33 localhost kernel:     TERM=linux
Oct 24 19:36:33 localhost kernel:     BOOT_IMAGE=/boot/vmlinuz-5.14.14-xanmod2-1-default
Oct 24 19:36:33 localhost kernel:     splash=silent
Oct 24 19:36:33 localhost kernel: efivarfs: module verification failed: signature and/or required key missing - tainting kernel
Oct 24 19:36:33 localhost systemd[1]: systemd 249.5+suse.47.g8521f8d22f running in system mode (+PAM +AUDIT +SELINUX +APPARMOR -IMA -SMACK +SECCOMP +GCRYPT +GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 -IDN -IPTC +KMOD +LIBCRYPTSETUP +LIBFDISK +PCRE2 +PWQUALITY +P11KIT +QRENCODE +BZIP2 +LZ4 +XZ +ZLIB +ZSTD -XKBCOMMON +UTMP +SYSVINIT default-hierarchy=unified)
Oct 24 19:36:33 localhost systemd[1]: Detected architecture x86-64.
Oct 24 19:36:33 localhost systemd[1]: Running in initial RAM disk.
Oct 24 19:36:33 localhost systemd[1]: No hostname configured, using default hostname.
Oct 24 19:36:33 localhost systemd[1]: Hostname set to <localhost>.
Oct 24 19:36:33 localhost systemd[1]: /usr/lib/systemd/system/plymouth-start.service:15: Unit configured to use KillMode=none. This is unsafe, as it disables systemd's process lifecycle management for the service. Please update your service to use a safer KillMode=, such as 'mixed' or 'control-group'. Support for KillMode=none is deprecated and will eventually be removed.
Oct 24 19:36:33 localhost systemd[1]: Queued start job for default target Initrd Default Target.
Oct 24 19:36:33 localhost systemd[1]: Reached target Initrd /usr File System.
Oct 24 19:36:33 localhost systemd[1]: Reached target Local File Systems.
Oct 24 19:36:33 localhost systemd[1]: Reached target Slice Units.
Oct 24 19:36:33 localhost systemd[1]: Reached target Swaps.
Oct 24 19:36:33 localhost systemd[1]: Reached target Timer Units.
Oct 24 19:36:33 localhost systemd[1]: Listening on Journal Socket (/dev/log).
Oct 24 19:36:33 localhost systemd[1]: Listening on Journal Socket.
Oct 24 19:36:33 localhost systemd[1]: Listening on udev Control Socket.
Oct 24 19:36:33 localhost systemd[1]: Listening on udev Kernel Socket.
Oct 24 19:36:33 localhost systemd[1]: Reached target Socket Units.
Oct 24 19:36:33 localhost systemd[1]: Started Entropy Daemon based on the HAVEGE algorithm.
Oct 24 19:36:33 localhost systemd[1]: Starting Create List of Static Device Nodes...
Oct 24 19:36:33 localhost systemd[1]: Starting Journal Service...
Oct 24 19:36:33 localhost systemd[1]: Starting Load Kernel Modules...
Oct 24 19:36:33 localhost systemd[1]: Starting Setup Virtual Console...
Oct 24 19:36:33 localhost systemd[1]: Finished Create List of Static Device Nodes.
Oct 24 19:36:33 localhost systemd[1]: Starting Create Static Device Nodes in /dev...
Oct 24 19:36:33 localhost systemd[1]: Finished Create Static Device Nodes in /dev.
Oct 24 19:36:33 localhost kernel: alua: device handler registered
Oct 24 19:36:33 localhost kernel: emc: device handler registered
Oct 24 19:36:33 localhost kernel: rdac: device handler registered
Oct 24 19:36:33 localhost kernel: device-mapper: uevent: version 1.0.3
Oct 24 19:36:33 localhost kernel: device-mapper: ioctl: 4.45.0-ioctl (2021-03-22) initialised: dm-devel@redhat.com
Oct 24 19:36:33 localhost kernel: sd 0:0:0:0: Attached scsi generic sg0 type 0
Oct 24 19:36:33 localhost kernel: sd 2:0:0:0: Attached scsi generic sg1 type 0
Oct 24 19:36:33 localhost kernel: sd 6:0:0:0: Attached scsi generic sg2 type 0
Oct 24 19:36:33 localhost systemd[1]: Finished Load Kernel Modules.
Oct 24 19:36:33 localhost systemd[1]: Starting Apply Kernel Variables...
Oct 24 19:36:33 localhost systemd[1]: Finished Apply Kernel Variables.
Oct 24 19:36:33 localhost systemd-journald[359]: Journal started
Oct 24 19:36:33 localhost systemd-journald[359]: Runtime Journal (/run/log/journal/30170ff3811249a89c4972a6cdbcd282) is 8.0M, max 639.9M, 631.9M free.
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'msr'
Oct 24 19:36:33 localhost haveged[357]: haveged: command socket is listening at fd 3
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'scsi_dh_alua'
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'scsi_dh_emc'
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'scsi_dh_rdac'
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'dm_multipath'
Oct 24 19:36:33 localhost systemd-modules-load[360]: Inserted module 'sg'
Oct 24 19:36:33 localhost systemd-sysctl[371]: Couldn't write '1' to 'net/ipv6/conf/default/use_tempaddr', ignoring: No such file or directory
Oct 24 19:36:33 localhost systemd-sysctl[371]: Couldn't write '0' to 'net/ipv6/conf/all/accept_redirects', ignoring: No such file or directory
Oct 24 19:36:33 localhost systemd-sysctl[371]: Couldn't write '0' to 'net/ipv6/conf/default/accept_redirects', ignoring: No such file or directory
Oct 24 19:36:33 localhost systemd[1]: Starting Create Volatile Files and Directories...
Oct 24 19:36:33 localhost systemd[1]: Started Journal Service.
Oct 24 19:36:33 localhost systemd[1]: Finished Create Volatile Files and Directories.
Oct 24 19:36:33 localhost systemd[1]: Finished Setup Virtual Console.
Oct 24 19:36:33 localhost systemd[1]: Starting dracut ask for additional cmdline parameters...
Oct 24 19:36:33 localhost systemd[1]: Finished dracut ask for additional cmdline parameters.
Oct 24 19:36:33 localhost systemd[1]: Starting dracut cmdline hook...
Oct 24 19:36:33 localhost dracut-cmdline[386]: dracut-dracut-055+suse.129.g7d8c3ce3-1.1
Oct 24 19:36:33 localhost dracut-cmdline[386]: Using kernel command line parameters:  root=UUID=b53e239d-b210-494f-986f-ccc63190e2ec rootfstype=xfs rootflags=rw,noatime,attr2,inode64,logbufs=8,logbsize=32k,noquota   BOOT_IMAGE=/boot/vmlinuz-5.14.14-xanmod2-1-default root=UUID=b53e239d-b210-494f-986f-ccc63190e2ec splash=silent quiet mitigations=off processor.max_cstate=5 idle=nomwait nowatchdog ipv6.disable=1
Oct 24 19:36:33 localhost systemd[1]: Finished dracut cmdline hook.
Oct 24 19:36:33 localhost systemd[1]: Starting dracut pre-udev hook...
Oct 24 19:36:33 localhost systemd[1]: Finished dracut pre-udev hook.
Oct 24 19:36:33 localhost systemd[1]: Starting Rule-based Manager for Device Events and Files...
Oct 24 19:36:33 localhost systemd[1]: Started Rule-based Manager for Device Events and Files.
Oct 24 19:36:33 localhost systemd[1]: Condition check resulted in dracut pre-trigger hook being skipped.
Oct 24 19:36:33 localhost systemd[1]: Starting Coldplug All udev Devices...
Oct 24 19:36:33 localhost systemd[1]: Finished Coldplug All udev Devices.
Oct 24 19:36:33 localhost systemd[1]: Reached target System Initialization.
Oct 24 19:36:33 localhost systemd[1]: Starting dracut initqueue hook...
Oct 24 19:36:33 localhost systemd[1]: Starting Show Plymouth Boot Screen...
Oct 24 19:36:33 localhost systemd[1]: Received SIGRTMIN+20 from PID 490 (plymouthd).
Oct 24 19:36:33 localhost kernel: nvme nvme0: pci function 0000:01:00.0
Oct 24 19:36:33 localhost kernel: ACPI: bus type USB registered
Oct 24 19:36:33 localhost kernel: nvme nvme1: pci function 0000:04:00.0
Oct 24 19:36:33 localhost kernel: usbcore: registered new interface driver usbfs
Oct 24 19:36:33 localhost kernel: usbcore: registered new interface driver hub
Oct 24 19:36:33 localhost kernel: usbcore: registered new device driver usb
Oct 24 19:36:33 localhost kernel: sp5100_tco: SP5100/SB800 TCO WatchDog Timer Driver
Oct 24 19:36:33 localhost kernel: sp5100-tco sp5100-tco: Using 0xfed80b00 for watchdog MMIO address
Oct 24 19:36:33 localhost kernel: sp5100-tco sp5100-tco: Watchdog hardware is disabled
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: new USB bus registered, assigned bus number 1
Oct 24 19:36:33 localhost kernel: ccp 0000:0b:00.1: enabling device (0000 -> 0002)
Oct 24 19:36:33 localhost kernel: ccp 0000:0b:00.1: ccp: unable to access the device: you might be running a broken BIOS.
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: hcc params 0x0278ffe5 hci version 0x110 quirks 0x0000000000000410
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: new USB bus registered, assigned bus number 2
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.1: Host supports USB 3.1 Enhanced SuperSpeed
Oct 24 19:36:33 localhost kernel: usb usb1: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb1: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb1: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb1: SerialNumber: 0000:06:00.1
Oct 24 19:36:33 localhost kernel: hub 1-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 1-0:1.0: 6 ports detected
Oct 24 19:36:33 localhost kernel: usb usb2: We don't know the algorithms for LPM for this host, disabling LPM.
Oct 24 19:36:33 localhost kernel: usb usb2: New USB device found, idVendor=1d6b, idProduct=0003, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb2: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb2: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb2: SerialNumber: 0000:06:00.1
Oct 24 19:36:33 localhost kernel: hub 2-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 2-0:1.0: 4 ports detected
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: new USB bus registered, assigned bus number 3
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: hcc params 0x0278ffe5 hci version 0x110 quirks 0x0000000000000410
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: new USB bus registered, assigned bus number 4
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:06:00.3: Host supports USB 3.1 Enhanced SuperSpeed
Oct 24 19:36:33 localhost kernel: usb usb3: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb3: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb3: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb3: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb3: SerialNumber: 0000:06:00.3
Oct 24 19:36:33 localhost kernel: hub 3-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 3-0:1.0: 6 ports detected
Oct 24 19:36:33 localhost kernel: nvme nvme0: missing or invalid SUBNQN field.
Oct 24 19:36:33 localhost kernel: nvme nvme0: Shutdown timeout set to 8 seconds
Oct 24 19:36:33 localhost kernel: usb usb4: We don't know the algorithms for LPM for this host, disabling LPM.
Oct 24 19:36:33 localhost kernel: usb usb4: New USB device found, idVendor=1d6b, idProduct=0003, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb4: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb4: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb4: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb4: SerialNumber: 0000:06:00.3
Oct 24 19:36:33 localhost kernel: hub 4-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 4-0:1.0: 4 ports detected
Oct 24 19:36:33 localhost kernel: nvme nvme1: missing or invalid SUBNQN field.
Oct 24 19:36:33 localhost kernel: nvme nvme1: Shutdown timeout set to 8 seconds
Oct 24 19:36:33 localhost kernel: usb: port power management may be unreliable
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: new USB bus registered, assigned bus number 5
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: hcc params 0x0278ffe5 hci version 0x110 quirks 0x0000000000000410
Oct 24 19:36:33 localhost kernel: cryptd: max_cpu_qlen set to 1000
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: new USB bus registered, assigned bus number 6
Oct 24 19:36:33 localhost kernel: xhci_hcd 0000:0b:00.3: Host supports USB 3.1 Enhanced SuperSpeed
Oct 24 19:36:33 localhost kernel: usb usb5: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb5: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb5: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb5: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb5: SerialNumber: 0000:0b:00.3
Oct 24 19:36:33 localhost kernel: hub 5-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 5-0:1.0: 4 ports detected
Oct 24 19:36:33 localhost kernel: usb usb6: We don't know the algorithms for LPM for this host, disabling LPM.
Oct 24 19:36:33 localhost kernel: usb usb6: New USB device found, idVendor=1d6b, idProduct=0003, bcdDevice= 5.14
Oct 24 19:36:33 localhost kernel: usb usb6: New USB device strings: Mfr=3, Product=2, SerialNumber=1
Oct 24 19:36:33 localhost kernel: usb usb6: Product: xHCI Host Controller
Oct 24 19:36:33 localhost kernel: usb usb6: Manufacturer: Linux 5.14.14-xanmod2-1-default xhci-hcd
Oct 24 19:36:33 localhost kernel: usb usb6: SerialNumber: 0000:0b:00.3
Oct 24 19:36:33 localhost kernel: AMD-Vi: AMD IOMMUv2 driver by Joerg Roedel <jroedel@suse.de>
Oct 24 19:36:33 localhost kernel: hub 6-0:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 6-0:1.0: 4 ports detected
Oct 24 19:36:33 localhost kernel: AVX2 version of gcm_enc/dec engaged.
Oct 24 19:36:33 localhost kernel: AES CTR mode by8 optimization enabled
Oct 24 19:36:33 localhost systemd[1]: Started Show Plymouth Boot Screen.
Oct 24 19:36:33 localhost systemd[1]: Condition check resulted in Dispatch Password Requests to Console Directory Watch being skipped.
Oct 24 19:36:33 localhost systemd[1]: Started Forward Password Requests to Plymouth Directory Watch.
Oct 24 19:36:33 localhost systemd[1]: Reached target Path Units.
Oct 24 19:36:33 localhost systemd[1]: Reached target Basic System.
Oct 24 19:36:33 localhost kernel: tsc: Refined TSC clocksource calibration: 3699.998 MHz
Oct 24 19:36:33 localhost kernel: clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x6aaaa638e3b, max_idle_ns: 881590585313 ns
Oct 24 19:36:33 localhost kernel: clocksource: Switched to clocksource tsc
Oct 24 19:36:33 localhost kernel: [drm] amdgpu kernel modesetting enabled.
Oct 24 19:36:33 localhost kernel: amdgpu: Ignoring ACPI CRAT on non-APU system
Oct 24 19:36:33 localhost kernel: amdgpu: Virtual CRAT table created for CPU
Oct 24 19:36:33 localhost kernel: amdgpu: Topology: Add CPU node
Oct 24 19:36:33 localhost kernel: checking generic (d0000000 300000) vs hw (d0000000 10000000)
Oct 24 19:36:33 localhost kernel: fb0: switching to amdgpudrmfb from EFI VGA
Oct 24 19:36:33 localhost kernel: Console: switching to colour dummy device 80x25
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: vgaarb: deactivate vga console
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: enabling device (0006 -> 0007)
Oct 24 19:36:33 localhost kernel: [drm] initializing kernel modesetting (POLARIS10 0x1002:0x67DF 0x1DA2:0xE343 0xEF).
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: Trusted Memory Zone (TMZ) feature not supported
Oct 24 19:36:33 localhost kernel: [drm] register mmio base: 0xFCE00000
Oct 24 19:36:33 localhost kernel: [drm] register mmio size: 262144
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 0 <vi_common>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 1 <gmc_v8_0>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 2 <tonga_ih>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 3 <gfx_v8_0>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 4 <sdma_v3_0>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 5 <powerplay>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 6 <dm>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 7 <uvd_v6_0>
Oct 24 19:36:33 localhost kernel: [drm] add ip block number 8 <vce_v3_0>
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: Fetched VBIOS from VFCT
Oct 24 19:36:33 localhost kernel: amdgpu: ATOM BIOS: 113-D00035-L01
Oct 24 19:36:33 localhost kernel: [drm] UVD is enabled in VM mode
Oct 24 19:36:33 localhost kernel: [drm] UVD ENC is enabled in VM mode
Oct 24 19:36:33 localhost kernel: [drm] VCE enabled in VM mode
Oct 24 19:36:33 localhost kernel: [drm] vm size is 128 GB, 2 levels, block size is 10-bit, fragment size is 9-bit
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: VRAM: 4096M 0x000000F400000000 - 0x000000F4FFFFFFFF (4096M used)
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: GART: 256M 0x000000FF00000000 - 0x000000FF0FFFFFFF
Oct 24 19:36:33 localhost kernel: [drm] Detected VRAM RAM=4096M, BAR=256M
Oct 24 19:36:33 localhost kernel: [drm] RAM width 256bits GDDR5
Oct 24 19:36:33 localhost kernel: [drm] amdgpu: 4096M of VRAM memory ready
Oct 24 19:36:33 localhost kernel: [drm] amdgpu: 4096M of GTT memory ready.
Oct 24 19:36:33 localhost kernel: [drm] GART: num cpu pages 65536, num gpu pages 65536
Oct 24 19:36:33 localhost kernel: nvme nvme0: 32/0/0 default/read/poll queues
Oct 24 19:36:33 localhost kernel: [drm] PCIE GART of 256M enabled (table at 0x000000F400300000).
Oct 24 19:36:33 localhost kernel: [drm] Chained IB support enabled!
Oct 24 19:36:33 localhost kernel: nvme nvme1: 32/0/0 default/read/poll queues
Oct 24 19:36:33 localhost kernel:  nvme0n1: p1 p2
Oct 24 19:36:33 localhost kernel:  nvme1n1: p1 p2 p3 p4 p5 p6
Oct 24 19:36:33 localhost kernel: amdgpu: hwmgr_sw_init smu backed is polaris10_smu
Oct 24 19:36:33 localhost systemd[1]: Found device Samsung SSD 970 EVO 250GB 6.
Oct 24 19:36:33 localhost systemd[1]: Found device Samsung SSD 970 EVO 250GB 5.
Oct 24 19:36:33 localhost kernel: [drm] Found UVD firmware Version: 1.130 Family ID: 16
Oct 24 19:36:33 localhost systemd[1]: Reached target Initrd Root Device.
Oct 24 19:36:33 localhost kernel: [drm] Found VCE firmware Version: 53.26 Binary ID: 3
Oct 24 19:36:33 localhost kernel: [drm] Display Core initialized with v3.2.141!
Oct 24 19:36:33 localhost kernel: usb 1-3: new high-speed USB device number 2 using xhci_hcd
Oct 24 19:36:33 localhost kernel: usb 5-3: new high-speed USB device number 2 using xhci_hcd
Oct 24 19:36:33 localhost kernel: usb 3-4: new full-speed USB device number 2 using xhci_hcd
Oct 24 19:36:33 localhost kernel: [drm] UVD and UVD ENC initialized successfully.
Oct 24 19:36:33 localhost kernel: [drm] VCE initialized successfully.
Oct 24 19:36:33 localhost kernel: kfd kfd: amdgpu: Allocated 3969056 bytes on gart
Oct 24 19:36:33 localhost kernel: usb 1-3: New USB device found, idVendor=045b, idProduct=0209, bcdDevice= 1.00
Oct 24 19:36:33 localhost kernel: usb 1-3: New USB device strings: Mfr=0, Product=0, SerialNumber=0
Oct 24 19:36:33 localhost kernel: amdgpu: SRAT table not found
Oct 24 19:36:33 localhost kernel: amdgpu: Virtual CRAT table created for GPU
Oct 24 19:36:33 localhost kernel: amdgpu: Topology: Add dGPU node [0x67df:0x1002]
Oct 24 19:36:33 localhost kernel: kfd kfd: amdgpu: added device 1002:67df
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: SE 4, SH per SE 1, CU per SH 9, active_cu_number 32
Oct 24 19:36:33 localhost kernel: [drm] fb mappable at 0xD0830000
Oct 24 19:36:33 localhost kernel: [drm] vram apper at 0xD0000000
Oct 24 19:36:33 localhost kernel: [drm] size 9216000
Oct 24 19:36:33 localhost kernel: [drm] fb depth is 24
Oct 24 19:36:33 localhost kernel: [drm]    pitch is 7680
Oct 24 19:36:33 localhost kernel: fbcon: amdgpu (fb0) is primary device
Oct 24 19:36:33 localhost kernel: usb 5-3: New USB device found, idVendor=30be, idProduct=0100, bcdDevice= 1.02
Oct 24 19:36:33 localhost kernel: usb 5-3: New USB device strings: Mfr=1, Product=2, SerialNumber=0
Oct 24 19:36:33 localhost kernel: usb 5-3: Product: I'm Fulla Schiit
Oct 24 19:36:33 localhost kernel: usb 5-3: Manufacturer: Schiit Audio
Oct 24 19:36:33 localhost kernel: usb 3-4: config 1 has an invalid interface number: 2 but max is 1
Oct 24 19:36:33 localhost kernel: usb 3-4: config 1 has no interface number 1
Oct 24 19:36:33 localhost kernel: usbcore: registered new interface driver usbhid
Oct 24 19:36:33 localhost kernel: usbhid: USB HID core driver
Oct 24 19:36:33 localhost kernel: input: Schiit Audio I'm Fulla Schiit as /devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-3/5-3:1.3/0003:30BE:0100.0001/input/input0
Oct 24 19:36:33 localhost kernel: usb 3-4: New USB device found, idVendor=0b05, idProduct=18f3, bcdDevice= 1.00
Oct 24 19:36:33 localhost kernel: usb 3-4: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Oct 24 19:36:33 localhost kernel: usb 3-4: Product: AURA LED Controller
Oct 24 19:36:33 localhost kernel: usb 3-4: Manufacturer: AsusTek Computer Inc.
Oct 24 19:36:33 localhost kernel: usb 3-4: SerialNumber: 9876543210
Oct 24 19:36:33 localhost kernel: hub 1-3:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 1-3:1.0: 4 ports detected
Oct 24 19:36:33 localhost kernel: hid-generic 0003:0B05:18F3.0002: hiddev96,hidraw0: USB HID v1.11 Device [AsusTek Computer Inc. AURA LED Controller] on usb-0000:06:00.3-4/input2
Oct 24 19:36:33 localhost kernel: Console: switching to colour frame buffer device 240x75
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: [drm] fb0: amdgpu frame buffer device
Oct 24 19:36:33 localhost kernel: hid-generic 0003:30BE:0100.0001: input,hidraw1: USB HID v1.00 Device [Schiit Audio I'm Fulla Schiit] on usb-0000:0b:00.3-3/input3
Oct 24 19:36:33 localhost kernel: amdgpu 0000:09:00.0: amdgpu: Using BACO for runtime pm
Oct 24 19:36:33 localhost kernel: [drm] Initialized amdgpu 3.42.0 20150101 for 0000:09:00.0 on minor 0
Oct 24 19:36:33 localhost kernel: usb 2-3: new SuperSpeed USB device number 2 using xhci_hcd
Oct 24 19:36:33 localhost systemd[1]: Finished dracut initqueue hook.
Oct 24 19:36:33 localhost systemd[1]: Reached target Preparation for Remote File Systems.
Oct 24 19:36:33 localhost systemd[1]: Reached target Remote File Systems.
Oct 24 19:36:33 localhost systemd[1]: Condition check resulted in dracut pre-mount hook being skipped.
Oct 24 19:36:33 localhost systemd[1]: Starting File System Check on /dev/disk/by-uuid/b53e239d-b210-494f-986f-ccc63190e2ec...
Oct 24 19:36:33 localhost kernel: usb 2-3: New USB device found, idVendor=045b, idProduct=0210, bcdDevice= 1.00
Oct 24 19:36:33 localhost kernel: usb 2-3: New USB device strings: Mfr=0, Product=0, SerialNumber=0
Oct 24 19:36:33 localhost kernel: usb 5-4: new full-speed USB device number 3 using xhci_hcd
Oct 24 19:36:33 localhost systemd-fsck[653]: /usr/sbin/fsck.xfs: XFS file system.
Oct 24 19:36:33 localhost systemd[1]: Finished File System Check on /dev/disk/by-uuid/b53e239d-b210-494f-986f-ccc63190e2ec.
Oct 24 19:36:33 localhost systemd[1]: Mounting /sysroot...
Oct 24 19:36:33 localhost kernel: usb 3-5: new high-speed USB device number 3 using xhci_hcd
Oct 24 19:36:33 localhost kernel: hub 2-3:1.0: USB hub found
Oct 24 19:36:33 localhost kernel: hub 2-3:1.0: 4 ports detected
Oct 24 19:36:34 localhost kernel: SGI XFS with ACLs, security attributes, quota, no debug enabled
Oct 24 19:36:34 localhost kernel: XFS (nvme1n1p6): Mounting V5 Filesystem
Oct 24 19:36:34 localhost kernel: XFS (nvme1n1p6): Ending clean mount
Oct 24 19:36:34 localhost systemd[1]: Mounted /sysroot.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in OSTree Prepare OS/ being skipped.
Oct 24 19:36:34 localhost systemd[1]: Reached target Initrd Root File System.
Oct 24 19:36:34 localhost systemd[1]: Starting Reload Configuration from the Real Root...
Oct 24 19:36:34 localhost systemd[1]: Reloading.
Oct 24 19:36:34 localhost kernel: usb 1-5: new high-speed USB device number 3 using xhci_hcd
Oct 24 19:36:34 localhost systemd[1]: /usr/lib/systemd/system/plymouth-start.service:15: Unit configured to use KillMode=none. This is unsafe, as it disables systemd's process lifecycle management for the service. Please update your service to use a safer KillMode=, such as 'mixed' or 'control-group'. Support for KillMode=none is deprecated and will eventually be removed.
Oct 24 19:36:34 localhost kernel: usb 5-4: New USB device found, idVendor=1532, idProduct=005b, bcdDevice= 2.00
Oct 24 19:36:34 localhost kernel: usb 5-4: New USB device strings: Mfr=1, Product=2, SerialNumber=0
Oct 24 19:36:34 localhost kernel: usb 5-4: Product: Razer Abyssus V2
Oct 24 19:36:34 localhost kernel: usb 5-4: Manufacturer: Razer
Oct 24 19:36:34 localhost systemd[1]: initrd-parse-etc.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Reload Configuration from the Real Root.
Oct 24 19:36:34 localhost systemd[1]: Reached target Initrd File Systems.
Oct 24 19:36:34 localhost systemd[1]: Reached target Initrd Default Target.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in dracut mount hook being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in dracut pre-pivot and cleanup hook being skipped.
Oct 24 19:36:34 localhost systemd[1]: Starting Cleaning Up and Shutting Down Daemons...
Oct 24 19:36:34 localhost kernel: usb 3-5: New USB device found, idVendor=1e71, idProduct=3008, bcdDevice= 5.07
Oct 24 19:36:34 localhost kernel: usb 3-5: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Oct 24 19:36:34 localhost kernel: usb 3-5: Product: NZXT KrakenZ Device
Oct 24 19:36:34 localhost kernel: usb 3-5: Manufacturer: NZXT Inc.
Oct 24 19:36:34 localhost kernel: usb 3-5: SerialNumber: 205A316D3456
Oct 24 19:36:34 localhost systemd[1]: Stopped target Initrd Default Target.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Basic System.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Initrd Root Device.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Initrd /usr File System.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Path Units.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Remote File Systems.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Preparation for Remote File Systems.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Slice Units.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Socket Units.
Oct 24 19:36:34 localhost systemd[1]: Stopped target System Initialization.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Swaps.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Timer Units.
Oct 24 19:36:34 localhost systemd[1]: dracut-initqueue.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped dracut initqueue hook.
Oct 24 19:36:34 localhost systemd[1]: Starting Tell haveged about new root...
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in OSTree Prepare OS/ being skipped.
Oct 24 19:36:34 localhost systemd[1]: Starting Plymouth switch root service...
Oct 24 19:36:34 localhost systemd[1]: systemd-sysctl.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Apply Kernel Variables.
Oct 24 19:36:34 localhost systemd[1]: systemd-modules-load.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Load Kernel Modules.
Oct 24 19:36:34 localhost systemd[1]: systemd-tmpfiles-setup.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Create Volatile Files and Directories.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Local File Systems.
Oct 24 19:36:34 localhost systemd[1]: systemd-udev-trigger.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Coldplug All udev Devices.
Oct 24 19:36:34 localhost systemd[1]: Stopping Rule-based Manager for Device Events and Files...
Oct 24 19:36:34 localhost systemd[1]: initrd-cleanup.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Cleaning Up and Shutting Down Daemons.
Oct 24 19:36:34 localhost systemd[1]: haveged-switch-root.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Tell haveged about new root.
Oct 24 19:36:34 localhost kernel: hid-generic 0003:1E71:3008.0003: hiddev97,hidraw2: USB HID v1.11 Device [NZXT Inc. NZXT KrakenZ Device] on usb-0000:06:00.3-5/input1
Oct 24 19:36:34 localhost kernel: input: Razer Razer Abyssus V2 as /devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-4/5-4:1.0/0003:1532:005B.0004/input/input1
Oct 24 19:36:34 localhost kernel: hid-generic 0003:1532:005B.0004: input,hidraw3: USB HID v1.11 Mouse [Razer Razer Abyssus V2] on usb-0000:0b:00.3-4/input0
Oct 24 19:36:34 localhost haveged[357]: haveged: command socket is listening at fd 3
Oct 24 19:36:34 localhost haveged[357]: haveged: Couldn't get poolsize
Oct 24 19:36:34 localhost systemd[1]: haveged.service: Main process exited, code=exited, status=1/FAILURE
Oct 24 19:36:34 localhost systemd[1]: haveged.service: Failed with result 'exit-code'.
Oct 24 19:36:34 localhost kernel: input: Razer Razer Abyssus V2 Keyboard as /devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-4/5-4:1.1/0003:1532:005B.0005/input/input2
Oct 24 19:36:34 localhost systemd[1]: Finished Plymouth switch root service.
Oct 24 19:36:34 localhost kernel: input: Razer Razer Abyssus V2 as /devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-4/5-4:1.1/0003:1532:005B.0005/input/input3
Oct 24 19:36:34 localhost kernel: hid-generic 0003:1532:005B.0005: input,hidraw4: USB HID v1.11 Keyboard [Razer Razer Abyssus V2] on usb-0000:0b:00.3-4/input1
Oct 24 19:36:34 localhost kernel: input: Razer Razer Abyssus V2 as /devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-4/5-4:1.2/0003:1532:005B.0006/input/input4
Oct 24 19:36:34 localhost kernel: usb 1-5: New USB device found, idVendor=05e3, idProduct=0610, bcdDevice=60.52
Oct 24 19:36:34 localhost kernel: usb 1-5: New USB device strings: Mfr=0, Product=1, SerialNumber=0
Oct 24 19:36:34 localhost kernel: usb 1-5: Product: USB2.0 Hub
Oct 24 19:36:34 localhost kernel: hid-generic 0003:1532:005B.0006: input,hidraw5: USB HID v1.11 Keyboard [Razer Razer Abyssus V2] on usb-0000:0b:00.3-4/input2
Oct 24 19:36:34 localhost systemd[1]: haveged.service: Scheduled restart job, restart counter is at 1.
Oct 24 19:36:34 localhost systemd[1]: Stopped Entropy Daemon based on the HAVEGE algorithm.
Oct 24 19:36:34 localhost systemd[1]: Started Entropy Daemon based on the HAVEGE algorithm.
Oct 24 19:36:34 localhost systemd[1]: systemd-udevd.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Rule-based Manager for Device Events and Files.
Oct 24 19:36:34 localhost haveged[709]: haveged: command socket is listening at fd 3
Oct 24 19:36:34 localhost systemd[1]: systemd-udevd-control.socket: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Closed udev Control Socket.
Oct 24 19:36:34 localhost systemd[1]: systemd-udevd-kernel.socket: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Closed udev Kernel Socket.
Oct 24 19:36:34 localhost systemd[1]: dracut-pre-udev.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped dracut pre-udev hook.
Oct 24 19:36:34 localhost systemd[1]: dracut-cmdline.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped dracut cmdline hook.
Oct 24 19:36:34 localhost systemd[1]: dracut-cmdline-ask.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped dracut ask for additional cmdline parameters.
Oct 24 19:36:34 localhost systemd[1]: Starting Cleanup udev Database...
Oct 24 19:36:34 localhost systemd[1]: systemd-tmpfiles-setup-dev.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Create Static Device Nodes in /dev.
Oct 24 19:36:34 localhost systemd[1]: kmod-static-nodes.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Create List of Static Device Nodes.
Oct 24 19:36:34 localhost systemd[1]: initrd-udevadm-cleanup-db.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Cleanup udev Database.
Oct 24 19:36:34 localhost systemd[1]: Reached target Switch Root.
Oct 24 19:36:34 localhost systemd[1]: Starting Switch Root...
Oct 24 19:36:34 localhost systemd[1]: Switching root.
Oct 24 19:36:34 localhost kernel: hub 1-5:1.0: USB hub found
Oct 24 19:36:34 localhost kernel: hub 1-5:1.0: 4 ports detected
Oct 24 19:36:34 localhost kernel: usb 1-3.3: new full-speed USB device number 4 using xhci_hcd
Oct 24 19:36:34 localhost systemd-journald[359]: Journal stopped
Oct 24 19:36:34 localhost systemd-journald[359]: Received SIGTERM from PID 1 (systemd).
Oct 24 19:36:34 localhost systemd[1]: systemd 249.5+suse.47.g8521f8d22f running in system mode (+PAM +AUDIT +SELINUX +APPARMOR -IMA -SMACK +SECCOMP +GCRYPT +GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 -IDN -IPTC +KMOD +LIBCRYPTSETUP +LIBFDISK +PCRE2 +PWQUALITY +P11KIT +QRENCODE +BZIP2 +LZ4 +XZ +ZLIB +ZSTD -XKBCOMMON +UTMP +SYSVINIT default-hierarchy=unified)
Oct 24 19:36:34 localhost systemd[1]: Detected architecture x86-64.
Oct 24 19:36:34 localhost kernel: usb 1-3.3: New USB device found, idVendor=056d, idProduct=4008, bcdDevice=80.00
Oct 24 19:36:34 localhost kernel: usb 1-3.3: New USB device strings: Mfr=1, Product=2, SerialNumber=0
Oct 24 19:36:34 localhost kernel: usb 1-3.3: Product: EIZO USB HID Monitor
Oct 24 19:36:34 localhost kernel: usb 1-3.3: Manufacturer: EIZO
Oct 24 19:36:34 localhost systemd[1]: /usr/lib/systemd/system/plymouth-start.service:15: Unit configured to use KillMode=none. This is unsafe, as it disables systemd's process lifecycle management for the service. Please update your service to use a safer KillMode=, such as 'mixed' or 'control-group'. Support for KillMode=none is deprecated and will eventually be removed.
Oct 24 19:36:34 localhost kernel: hid-generic 0003:056D:4008.0007: hiddev98,hidraw6: USB HID v1.10 Device [EIZO EIZO USB HID Monitor] on usb-0000:06:00.1-3.3/input0
Oct 24 19:36:34 localhost systemd[1]: haveged.service: Main process exited, code=exited, status=1/FAILURE
Oct 24 19:36:34 localhost systemd[1]: haveged.service: Failed with result 'exit-code'.
Oct 24 19:36:34 localhost systemd[1]: Stopped Entropy Daemon based on the HAVEGE algorithm.
Oct 24 19:36:34 localhost systemd[1]: initrd-switch-root.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Switch Root.
Oct 24 19:36:34 localhost systemd[1]: systemd-journald.service: Scheduled restart job, restart counter is at 1.
Oct 24 19:36:34 localhost systemd[1]: Created slice Slice /system/getty.
Oct 24 19:36:34 localhost systemd[1]: Created slice Slice /system/modprobe.
Oct 24 19:36:34 localhost systemd[1]: Created slice Slice /system/systemd-fsck.
Oct 24 19:36:34 localhost systemd[1]: Created slice User and Session Slice.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Arbitrary Executable File Formats File System Automount Point being skipped.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Switch Root.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Initrd File Systems.
Oct 24 19:36:34 localhost systemd[1]: Stopped target Initrd Root File System.
Oct 24 19:36:34 localhost systemd[1]: Reached target Remote File Systems.
Oct 24 19:36:34 localhost systemd[1]: Reached target Slice Units.
Oct 24 19:36:34 localhost systemd[1]: Reached target Swaps.
Oct 24 19:36:34 localhost systemd[1]: Reached target System Time Set.
Oct 24 19:36:34 localhost systemd[1]: Reached target Local Verity Integrity Protected Volumes.
Oct 24 19:36:34 localhost systemd[1]: Listening on Device-mapper event daemon FIFOs.
Oct 24 19:36:34 localhost systemd[1]: Listening on initctl Compatibility Named Pipe.
Oct 24 19:36:34 localhost systemd[1]: Listening on udev Control Socket.
Oct 24 19:36:34 localhost systemd[1]: Listening on udev Kernel Socket.
Oct 24 19:36:34 localhost systemd[1]: Mounting Huge Pages File System...
Oct 24 19:36:34 localhost systemd[1]: Mounting POSIX Message Queue File System...
Oct 24 19:36:34 localhost systemd[1]: Mounting Kernel Debug File System...
Oct 24 19:36:34 localhost systemd[1]: Mounting Kernel Trace File System...
Oct 24 19:36:34 localhost systemd[1]: Mounting Temporary Directory /tmp...
Oct 24 19:36:34 localhost systemd[1]: Starting Load AppArmor profiles...
Oct 24 19:36:34 localhost systemd[1]: Starting Create List of Static Device Nodes...
Oct 24 19:36:34 localhost systemd[1]: Starting Load Kernel Module configfs...
Oct 24 19:36:34 localhost systemd[1]: Starting Load Kernel Module drm...
Oct 24 19:36:34 localhost systemd[1]: Starting Load Kernel Module fuse...
Oct 24 19:36:34 localhost systemd[1]: plymouth-start.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: plymouth-start.service: Unit process 490 (plymouthd) remains running after unit stopped.
Oct 24 19:36:34 localhost systemd[1]: Stopped Show Plymouth Boot Screen.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Dispatch Password Requests to Console Directory Watch being skipped.
Oct 24 19:36:34 localhost systemd[1]: Reached target Local Encrypted Volumes.
Oct 24 19:36:34 localhost systemd[1]: plymouth-switch-root.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped Plymouth switch root service.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Set Up Additional Binary Formats being skipped.
Oct 24 19:36:34 localhost systemd[1]: systemd-fsck-root.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Stopped File System Check on Root Device.
Oct 24 19:36:34 localhost systemd[1]: Stopped Journal Service.
Oct 24 19:36:34 localhost systemd[1]: Starting Journal Service...
Oct 24 19:36:34 localhost systemd[1]: Starting Load Kernel Modules...
Oct 24 19:36:34 localhost systemd[1]: Starting Remount Root and Kernel File Systems...
Oct 24 19:36:34 localhost systemd[1]: Starting Coldplug All udev Devices...
Oct 24 19:36:34 localhost kernel: xfs filesystem being remounted at / supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:34 localhost systemd-journald[744]: Journal started
Oct 24 19:36:34 localhost systemd-journald[744]: Runtime Journal (/run/log/journal/30170ff3811249a89c4972a6cdbcd282) is 8.0M, max 639.9M, 631.9M free.
Oct 24 19:36:34 localhost systemd[1]: Queued start job for default target Graphical Interface.
Oct 24 19:36:34 localhost systemd[1]: systemd-journald.service: Deactivated successfully.
Oct 24 19:36:34 localhost apparmor.systemd[738]: Restarting AppArmor
Oct 24 19:36:34 localhost apparmor.systemd[738]: Reloading AppArmor profiles
Oct 24 19:36:34 localhost apparmor.systemd[751]: Warning from stdin (line 1): Cache: failed to add read only location '/usr/share/apparmor/cache', does not contain valid cache directory for the specified feature set
Oct 24 19:36:34 localhost kernel: fuse: init (API version 7.34)
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:2): apparmor="STATUS" operation="profile_load" profile="unconfined" name="/usr/bin/lessopen.sh" pid=761 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:3): apparmor="STATUS" operation="profile_load" profile="unconfined" name="klogd" pid=758 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:4): apparmor="STATUS" operation="profile_load" profile="unconfined" name="dovecot-log" pid=773 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:5): apparmor="STATUS" operation="profile_load" profile="unconfined" name="dovecot-managesieve-login" pid=775 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:6): apparmor="STATUS" operation="profile_load" profile="unconfined" name="dovecot-managesieve" pid=774 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:7): apparmor="STATUS" operation="profile_load" profile="unconfined" name="dovecot-anvil" pid=763 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.529:8): apparmor="STATUS" operation="profile_load" profile="unconfined" name="dovecot-imap-login" pid=771 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.531:9): apparmor="STATUS" operation="profile_load" profile="unconfined" name="lsb_release" pid=754 comm="apparmor_parser"
Oct 24 19:36:34 localhost kernel: audit: type=1400 audit(1635096994.531:10): apparmor="STATUS" operation="profile_load" profile="unconfined" name="nvidia_modprobe" pid=755 comm="apparmor_parser"
Oct 24 19:36:34 localhost systemd[1]: Mounted Huge Pages File System.
Oct 24 19:36:34 localhost systemd[1]: Mounted POSIX Message Queue File System.
Oct 24 19:36:34 localhost systemd[1]: Mounted Kernel Debug File System.
Oct 24 19:36:34 localhost systemd[1]: Mounted Kernel Trace File System.
Oct 24 19:36:34 localhost systemd[1]: Mounted Temporary Directory /tmp.
Oct 24 19:36:34 localhost systemd[1]: Finished Load AppArmor profiles.
Oct 24 19:36:34 localhost systemd[1]: Finished Create List of Static Device Nodes.
Oct 24 19:36:34 localhost systemd[1]: modprobe@configfs.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Load Kernel Module configfs.
Oct 24 19:36:34 localhost systemd[1]: modprobe@drm.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Load Kernel Module drm.
Oct 24 19:36:34 localhost systemd[1]: modprobe@fuse.service: Deactivated successfully.
Oct 24 19:36:34 localhost systemd[1]: Finished Load Kernel Module fuse.
Oct 24 19:36:34 localhost systemd[1]: Started Journal Service.
Oct 24 19:36:34 localhost systemd[1]: Finished Load Kernel Modules.
Oct 24 19:36:34 localhost systemd[1]: Finished Remount Root and Kernel File Systems.
Oct 24 19:36:34 localhost systemd[1]: Mounting FUSE Control File System...
Oct 24 19:36:34 localhost systemd[1]: Mounting Kernel Configuration File System...
Oct 24 19:36:34 localhost systemd[1]: Starting Apply Kernel Variables for 5.14.14-xanmod2-1-default from /boot...
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Apply Kernel Variables for 5.14.14-xanmod2-1-default being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Wizard being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Rebuild Hardware Database being skipped.
Oct 24 19:36:34 localhost systemd[1]: Starting Flush Journal to Persistent Storage...
Oct 24 19:36:34 localhost systemd[1]: Starting Load/Save Random Seed...
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Create System Users being skipped.
Oct 24 19:36:34 localhost systemd[1]: Starting Create Static Device Nodes in /dev...
Oct 24 19:36:34 localhost systemd-sysctl[797]: Failed to open file '/boot/sysctl.conf-5.14.14-xanmod2-1-default', ignoring: No such file or directory
Oct 24 19:36:34 localhost systemd[1]: Mounted FUSE Control File System.
Oct 24 19:36:34 localhost systemd[1]: Mounted Kernel Configuration File System.
Oct 24 19:36:34 localhost systemd[1]: boot-sysctl.service: Main process exited, code=exited, status=1/FAILURE
Oct 24 19:36:34 localhost systemd[1]: boot-sysctl.service: Failed with result 'exit-code'.
Oct 24 19:36:34 localhost systemd[1]: Failed to start Apply Kernel Variables for 5.14.14-xanmod2-1-default from /boot.
Oct 24 19:36:34 localhost systemd[1]: Starting Apply Kernel Variables...
Oct 24 19:36:34 localhost systemd-journald[744]: Time spent on flushing to /var/log/journal/30170ff3811249a89c4972a6cdbcd282 is 67.032ms for 1386 entries.
Oct 24 19:36:34 localhost systemd-journald[744]: System Journal (/var/log/journal/30170ff3811249a89c4972a6cdbcd282) is 560.0M, max 4.0G, 3.4G free.
Oct 24 19:36:34 localhost kernel: usb 1-5.1: new low-speed USB device number 5 using xhci_hcd
Oct 24 19:36:34 localhost kernel: EXT4-fs (nvme0n1p1): mounted filesystem with ordered data mode. Opts: commit=60. Quota mode: none.
Oct 24 19:36:34 localhost kernel: input: Power Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0C:00/input/input5
Oct 24 19:36:34 localhost kernel: ACPI: button: Power Button [PWRB]
Oct 24 19:36:34 localhost kernel: input: Power Button as /devices/LNXSYSTM:00/LNXPWRBN:00/input/input6
Oct 24 19:36:34 localhost kernel: ACPI: button: Power Button [PWRF]
Oct 24 19:36:34 localhost kernel: acpi PNP0C14:02: duplicate WMI GUID 05901221-D566-11D1-B2F0-00A0C9062910 (first instance was on PNP0C14:01)
Oct 24 19:36:34 localhost kernel: acpi PNP0C14:03: duplicate WMI GUID 05901221-D566-11D1-B2F0-00A0C9062910 (first instance was on PNP0C14:01)
Oct 24 19:36:34 localhost kernel: acpi PNP0C14:04: duplicate WMI GUID 05901221-D566-11D1-B2F0-00A0C9062910 (first instance was on PNP0C14:01)
Oct 24 19:36:34 localhost kernel: acpi PNP0C14:05: duplicate WMI GUID 05901221-D566-11D1-B2F0-00A0C9062910 (first instance was on PNP0C14:01)
Oct 24 19:36:34 localhost systemd-sysctl[801]: Couldn't write '1' to 'net/ipv6/conf/default/use_tempaddr', ignoring: No such file or directory
Oct 24 19:36:34 localhost systemd-sysctl[801]: Couldn't write '0' to 'net/ipv6/conf/all/accept_redirects', ignoring: No such file or directory
Oct 24 19:36:34 localhost systemd-sysctl[801]: Couldn't write '0' to 'net/ipv6/conf/default/accept_redirects', ignoring: No such file or directory
Oct 24 19:36:34 localhost systemd-fsck[811]: /dev/nvme0n1p1: clean, 757310/19660800 files, 10262737/78643200 blocks
Oct 24 19:36:34 localhost systemd[1]: Finished Apply Kernel Variables.
Oct 24 19:36:34 localhost systemd-fsck[809]: fsck.fat 4.2 (2021-01-31)
Oct 24 19:36:34 localhost systemd-fsck[809]: /dev/nvme1n1p5: 3 files, 20/62465 clusters
Oct 24 19:36:34 localhost systemd[1]: Finished Load/Save Random Seed.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Complete being skipped.
Oct 24 19:36:34 localhost systemd[1]: Finished Create Static Device Nodes in /dev.
Oct 24 19:36:34 localhost systemd[1]: Reached target Preparation for Local File Systems.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Lock Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Runtime Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: Starting File System Check on /dev/disk/by-uuid/11c2079b-994c-47c7-a087-7bdf42c59b62...
Oct 24 19:36:34 localhost systemd[1]: Starting File System Check on /dev/disk/by-uuid/1E04-0105...
Oct 24 19:36:34 localhost systemd[1]: Starting File System Check on /dev/disk/by-uuid/fa530d85-2747-4be1-a534-d76228708ce0...
Oct 24 19:36:34 localhost systemd[1]: Starting Rule-based Manager for Device Events and Files...
Oct 24 19:36:34 localhost systemd[1]: Finished File System Check on /dev/disk/by-uuid/1E04-0105.
Oct 24 19:36:34 localhost systemd[1]: Mounting /boot/efi...
Oct 24 19:36:34 localhost systemd[1]: Finished Coldplug All udev Devices.
Oct 24 19:36:34 localhost systemd[1]: Finished File System Check on /dev/disk/by-uuid/11c2079b-994c-47c7-a087-7bdf42c59b62.
Oct 24 19:36:34 localhost systemd[1]: Mounting /media/x...
Oct 24 19:36:34 localhost systemd[1]: Mounted /boot/efi.
Oct 24 19:36:34 localhost systemd[1]: Mounted /media/x.
Oct 24 19:36:34 localhost systemd[1]: Started Rule-based Manager for Device Events and Files.
Oct 24 19:36:34 localhost systemd[1]: Finished Flush Journal to Persistent Storage.
Oct 24 19:36:34 localhost kernel: dca service started, version 1.12.1
Oct 24 19:36:34 localhost kernel: igb: Intel(R) Gigabit Ethernet Network Driver
Oct 24 19:36:34 localhost kernel: igb: Copyright (c) 2007-2014 Intel Corporation.
Oct 24 19:36:34 localhost systemd-fsck[891]: /usr/sbin/fsck.xfs: XFS file system.
Oct 24 19:36:34 localhost mtp-probe[892]: checking bus 3, device 2: "/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.3/usb3/3-4"
Oct 24 19:36:34 localhost mtp-probe[888]: checking bus 3, device 3: "/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.3/usb3/3-5"
Oct 24 19:36:34 localhost systemd[1]: Finished File System Check on /dev/disk/by-uuid/fa530d85-2747-4be1-a534-d76228708ce0.
Oct 24 19:36:34 localhost systemd[1]: Mounting /media/big...
Oct 24 19:36:34 localhost mtp-probe[892]: bus: 3, device: 2 was not an MTP device
Oct 24 19:36:34 localhost mtp-probe[888]: bus: 3, device: 3 was not an MTP device
Oct 24 19:36:34 localhost kernel: XFS (sda1): Mounting V5 Filesystem
Oct 24 19:36:34 localhost mtp-probe[904]: checking bus 1, device 4: "/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-3/1-3.3"
Oct 24 19:36:34 localhost mtp-probe[904]: bus: 1, device: 4 was not an MTP device
Oct 24 19:36:34 localhost mtp-probe[909]: checking bus 5, device 2: "/sys/devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-3"
Oct 24 19:36:34 localhost kernel: piix4_smbus 0000:00:14.0: SMBus Host Controller at 0xb00, revision 0
Oct 24 19:36:34 localhost kernel: piix4_smbus 0000:00:14.0: Using register 0x02 for SMBus port selection
Oct 24 19:36:34 localhost kernel: piix4_smbus 0000:00:14.0: Auxiliary SMBus Host Controller at 0xb20
Oct 24 19:36:34 localhost kernel: piix4_smbus 0000:00:14.0: SMBus region 0xb20 already in use!
Oct 24 19:36:34 localhost mtp-probe[911]: checking bus 5, device 3: "/sys/devices/pci0000:00/0000:00:08.1/0000:0b:00.3/usb5/5-4"
Oct 24 19:36:34 localhost mtp-probe[909]: bus: 5, device: 2 was not an MTP device
Oct 24 19:36:34 localhost mtp-probe[911]: bus: 5, device: 3 was not an MTP device
Oct 24 19:36:34 localhost kernel: input: PC Speaker as /devices/platform/pcspkr/input/input7
Oct 24 19:36:34 localhost kernel: pstore: Using crash dump compression: lzo
Oct 24 19:36:34 localhost kernel: pstore: Registered efi as persistent store backend
Oct 24 19:36:34 localhost kernel: mc: Linux media interface: v0.10
Oct 24 19:36:34 localhost kernel: pps pps0: new PPS source ptp0
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0: added PHC on eth0
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0: Intel(R) Gigabit Ethernet Network Connection
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0: eth0: (PCIe:2.5Gb/s:Width x1) fc:34:97:a2:d4:6d
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0: eth0: PBA No: FFFFFF-0FF
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0: Using MSI-X interrupts. 2 rx queue(s), 2 tx queue(s)
Oct 24 19:36:34 localhost systemd[1]: Started Entropy Daemon based on the HAVEGE algorithm.
Oct 24 19:36:34 localhost haveged[931]: haveged: command socket is listening at fd 3
Oct 24 19:36:34 localhost kernel: snd_hda_intel 0000:09:00.1: enabling device (0000 -> 0002)
Oct 24 19:36:34 localhost kernel: snd_hda_intel 0000:09:00.1: Force to non-snoop mode
Oct 24 19:36:34 localhost systemd-udevd[841]: Using default interface naming scheme 'v249'.
Oct 24 19:36:34 localhost kernel: snd_hda_intel 0000:09:00.1: bound 0000:09:00.0 (ops amdgpu_dm_audio_component_bind_ops [amdgpu])
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=3 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input8
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=7 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input9
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=8 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input10
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=9 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input11
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=10 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input12
Oct 24 19:36:34 localhost kernel: input: HDA ATI HDMI HDMI/DP,pcm=11 as /devices/pci0000:00/0000:00:03.1/0000:09:00.1/sound/card1/input13
Oct 24 19:36:34 localhost kernel: igb 0000:05:00.0 enp5s0: renamed from eth0
Oct 24 19:36:34 localhost systemd[1]: Listening on Load/Save RF Kill Switch Status /dev/rfkill Watch.
Oct 24 19:36:34 localhost kernel: intel_rapl_common: Found RAPL domain package
Oct 24 19:36:34 localhost kernel: intel_rapl_common: Found RAPL domain core
Oct 24 19:36:34 localhost kernel: asus_wmi: ASUS WMI generic driver loaded
Oct 24 19:36:34 localhost kernel: asus_wmi: Initialization: 0x0
Oct 24 19:36:34 localhost kernel: asus_wmi: BIOS WMI version: 0.9
Oct 24 19:36:34 localhost kernel: asus_wmi: SFUN value: 0x0
Oct 24 19:36:34 localhost kernel: eeepc-wmi eeepc-wmi: Detected ASUSWMI, use DCTS
Oct 24 19:36:34 localhost kernel: input: Eee PC WMI hotkeys as /devices/platform/eeepc-wmi/input/input14
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Arbitrary Executable File Formats File System Automount Point being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Lock Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Runtime Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: plymouth-start.service: Found left-over process 490 (plymouthd) in control group while starting unit. Ignoring.
Oct 24 19:36:34 localhost systemd[1]: This usually indicates unclean termination of a previous run, or service implementation deficiencies.
Oct 24 19:36:34 localhost systemd[1]: Starting Show Plymouth Boot Screen...
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Set Up Additional Binary Formats being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Wizard being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Complete being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Rebuild Hardware Database being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Create System Users being skipped.
Oct 24 19:36:34 localhost systemd[1]: Started Show Plymouth Boot Screen.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Dispatch Password Requests to Console Directory Watch being skipped.
Oct 24 19:36:34 localhost kernel: usbcore: registered new interface driver snd-usb-audio
Oct 24 19:36:34 localhost systemd-udevd[859]: controlC0: Process '/usr/sbin/alsactl restore 0' failed with exit code 99.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Dispatch Password Requests to Console Directory Watch being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Arbitrary Executable File Formats File System Automount Point being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Lock Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Runtime Directory being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Set Up Additional Binary Formats being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Wizard being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in First Boot Complete being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Rebuild Hardware Database being skipped.
Oct 24 19:36:34 localhost systemd[1]: Condition check resulted in Create System Users being skipped.
Oct 24 19:36:34 localhost systemd-udevd[853]: Using default interface naming scheme 'v249'.
Oct 24 19:36:34 localhost kernel: usb 1-5.1: New USB device found, idVendor=2516, idProduct=001a, bcdDevice= 1.04
Oct 24 19:36:34 localhost kernel: usb 1-5.1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
Oct 24 19:36:34 localhost kernel: usb 1-5.1: Product: Keyboard -- QuickFire XT
Oct 24 19:36:34 localhost kernel: usb 1-5.1: Manufacturer: CM Storm
Oct 24 19:36:34 localhost kernel: input: CM Storm Keyboard -- QuickFire XT as /devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-5/1-5.1/1-5.1:1.0/0003:2516:001A.0008/input/input15
Oct 24 19:36:34 localhost kernel: hid-generic 0003:2516:001A.0008: input,hidraw7: USB HID v1.10 Keyboard [CM Storm Keyboard -- QuickFire XT] on usb-0000:06:00.1-5.1/input0
Oct 24 19:36:34 localhost kernel: input: CM Storm Keyboard -- QuickFire XT Consumer Control as /devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-5/1-5.1/1-5.1:1.1/0003:2516:001A.0009/input/input16
Oct 24 19:36:34 localhost kernel: input: CM Storm Keyboard -- QuickFire XT System Control as /devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-5/1-5.1/1-5.1:1.1/0003:2516:001A.0009/input/input17
Oct 24 19:36:34 localhost kernel: hid-generic 0003:2516:001A.0009: input,hidraw8: USB HID v1.10 Device [CM Storm Keyboard -- QuickFire XT] on usb-0000:06:00.1-5.1/input1
Oct 24 19:36:34 localhost mtp-probe[1012]: checking bus 1, device 5: "/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-5/1-5.1"
Oct 24 19:36:34 localhost mtp-probe[1012]: bus: 1, device: 5 was not an MTP device
Oct 24 19:36:35 localhost mtp-probe[1018]: checking bus 1, device 5: "/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:08.0/0000:06:00.1/usb1/1-5/1-5.1"
Oct 24 19:36:35 localhost mtp-probe[1018]: bus: 1, device: 5 was not an MTP device
Oct 24 19:36:35 localhost kernel: XFS (sda1): Ending clean mount
Oct 24 19:36:35 localhost kernel: xfs filesystem being mounted at /media/big supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost systemd[1]: Mounted /media/big.
Oct 24 19:36:35 localhost systemd[1]: Reached target Local File Systems.
Oct 24 19:36:35 localhost systemd[1]: Starting Restore /run/initramfs on shutdown...
Oct 24 19:36:35 localhost systemd[1]: Starting Tell Plymouth To Write Out Runtime Data...
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Store a System Token in an EFI Variable being skipped.
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Commit a transient machine-id on disk being skipped.
Oct 24 19:36:35 localhost systemd[1]: Starting Create Volatile Files and Directories...
Oct 24 19:36:35 localhost systemd[1]: Finished Restore /run/initramfs on shutdown.
Oct 24 19:36:35 localhost systemd[1]: Finished Create Volatile Files and Directories.
Oct 24 19:36:35 localhost systemd[1]: Starting Security Auditing Service...
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Rebuild Journal Catalog being skipped.
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Update is Completed being skipped.
Oct 24 19:36:35 localhost systemd[1]: Received SIGRTMIN+20 from PID 490 (plymouthd).
Oct 24 19:36:35 localhost systemd[1]: Finished Tell Plymouth To Write Out Runtime Data.
Oct 24 19:36:35 localhost auditd[1023]: No plugins found, not dispatching events
Oct 24 19:36:35 localhost auditd[1023]: Init complete, auditd 3.0.5 listening for events (startup state enable)
Oct 24 19:36:35 localhost systemd[1]: Started Security Auditing Service.
Oct 24 19:36:35 localhost systemd[1]: Starting Record System Boot/Shutdown in UTMP...
Oct 24 19:36:35 localhost systemd[1]: Finished Record System Boot/Shutdown in UTMP.
Oct 24 19:36:35 localhost systemd[1]: Reached target System Initialization.
Oct 24 19:36:35 localhost systemd[1]: Started Watch /etc/sysconfig/btrfsmaintenance.
Oct 24 19:36:35 localhost systemd[1]: Started Watch for changes in CA certificates.
Oct 24 19:36:35 localhost systemd[1]: Started CUPS Scheduler.
Oct 24 19:36:35 localhost systemd[1]: Started Watch for changes in issue snippets.
Oct 24 19:36:35 localhost systemd[1]: Started Watch for changes in smartmontools sysconfig file.
Oct 24 19:36:35 localhost systemd[1]: Started Daily Cleanup of Snapper Snapshots.
Oct 24 19:36:35 localhost systemd[1]: Started Daily Cleanup of Temporary Directories.
Oct 24 19:36:35 localhost systemd[1]: Reached target Path Units.
Oct 24 19:36:35 localhost systemd[1]: Listening on Avahi mDNS/DNS-SD Stack Activation Socket.
Oct 24 19:36:35 localhost systemd[1]: Listening on CUPS Scheduler.
Oct 24 19:36:35 localhost systemd[1]: Listening on D-Bus System Message Bus Socket.
Oct 24 19:36:35 localhost systemd[1]: Listening on PC/SC Smart Card Daemon Activation Socket.
Oct 24 19:36:35 localhost systemd[1]: Reached target Socket Units.
Oct 24 19:36:35 localhost systemd[1]: Reached target Basic System.
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in YaST2 Second Stage being skipped.
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in YaST2 Firstboot being skipped.
Oct 24 19:36:35 localhost systemd[1]: Starting Save/Restore Sound Card State...
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Manage Sound Card State (restore and store) being skipped.
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Synchronize AppStream metadata from repositories into AS-cache being skipped.
Oct 24 19:36:35 localhost systemd[1]: Starting Avahi mDNS/DNS-SD Stack...
Oct 24 19:36:35 localhost systemd[1]: Started D-Bus System Message Bus.
Oct 24 19:36:35 localhost alsactl[1027]: alsa-lib main.c:1405:(snd_use_case_mgr_open) error: failed to import hw:0 use case configuration -2
Oct 24 19:36:35 localhost alsactl[1027]: No state is present for card Schiit
Oct 24 19:36:35 localhost alsactl[1027]: alsa-lib main.c:1405:(snd_use_case_mgr_open) error: failed to import hw:0 use case configuration -2
Oct 24 19:36:35 localhost alsactl[1027]: Found hardware: "USB-Audio" "USB Mixer" "USB30be:0100" "" ""
Oct 24 19:36:35 localhost alsactl[1027]: Hardware is initialized using a generic method
Oct 24 19:36:35 localhost alsactl[1027]: No state is present for card Schiit
Oct 24 19:36:35 localhost alsactl[1027]: alsa-lib parser.c:242:(error_node) UCM is not supported for this HDA model (HDA ATI HDMI at 0xfce60000 irq 153)
Oct 24 19:36:35 localhost alsactl[1027]: alsa-lib main.c:1405:(snd_use_case_mgr_open) error: failed to import hw:1 use case configuration -6
Oct 24 19:36:35 localhost systemd[1]: Started irqbalance daemon.
Oct 24 19:36:35 localhost systemd[1]: Starting Generate issue file for login session...
Oct 24 19:36:35 localhost systemd[1]: Starting Apply settings from /etc/sysconfig/keyboard...
Oct 24 19:36:35 localhost avahi-daemon[1028]: Found user 'avahi' (UID 499) and group 'avahi' (GID 499).
Oct 24 19:36:35 localhost avahi-daemon[1028]: Successfully dropped root privileges.
Oct 24 19:36:35 localhost avahi-daemon[1028]: avahi-daemon 0.8 starting up.
Oct 24 19:36:35 localhost systemd[1]: Starting Machine Check Exception Logging Daemon...
Oct 24 19:36:35 localhost systemd[1]: Starting AIO startup service...
Oct 24 19:36:35 localhost systemd[1]: Starting Name Service Cache Daemon...
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Auto-connect to subsystems on FC-NVME devices found during boot being skipped.
Oct 24 19:36:35 localhost systemd[1]: Starting Authorization Manager...
Oct 24 19:36:35 localhost systemd[1]: Starting Self Monitoring and Reporting Technology (SMART) Daemon...
Oct 24 19:36:35 localhost systemd[1]: Condition check resulted in Purge old kernels being skipped.
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/passwd` (1)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/group` (3)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost systemd[1]: Finished Save/Restore Sound Card State.
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/hosts` (4)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/resolv.conf` (5)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 disabled inotify-based monitoring for file `/etc/services': No such file or directory
Oct 24 19:36:35 localhost nscd[1052]: 1052 stat failed for file `/etc/services'; will try again later: No such file or directory
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/netgroup` (6)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost systemd[1]: Starting Load extra kernel modules for sound stuff...
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:35 localhost nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:35 localhost systemd[1]: issue-generator.service: Deactivated successfully.
Oct 24 19:36:35 localhost systemd[1]: Finished Generate issue file for login session.
Oct 24 19:36:35 localhost systemd[1]: Started Machine Check Exception Logging Daemon.
Oct 24 19:36:35 localhost systemd[1]: Started Name Service Cache Daemon.
Oct 24 19:36:35 localhost systemd[1]: Reached target Host and Network Name Lookups.
Oct 24 19:36:35 localhost systemd[1]: Reached target User and Group Name Lookups.
Oct 24 19:36:35 localhost systemd[1]: Starting User Login Management...
Oct 24 19:36:35 localhost systemd[1]: Finished Apply settings from /etc/sysconfig/keyboard.
Oct 24 19:36:35 localhost systemd[1]: sound-extra.service: Deactivated successfully.
Oct 24 19:36:35 localhost systemd[1]: Finished Load extra kernel modules for sound stuff.
Oct 24 19:36:35 localhost systemd[1]: Reached target Sound Card.
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/lib/systemd/linger supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost smartd[1051]: smartd 7.2 2021-06-06 r5225 [x86_64-linux-5.14.14-xanmod2-1-default] (SUSE RPM)
Oct 24 19:36:35 localhost smartd[1051]: Copyright (C) 2002-20, Bruce Allen, Christian Franke, www.smartmontools.org
Oct 24 19:36:35 localhost smartd[1051]: Opened configuration file /etc/smartd.conf
Oct 24 19:36:35 localhost smartd[1051]: Drive: DEVICESCAN, implied '-a' Directive on line 32 of file /etc/smartd.conf
Oct 24 19:36:35 localhost smartd[1051]: Configuration file /etc/smartd.conf was parsed, found DEVICESCAN, scanning devices
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda, type changed from 'scsi' to 'sat'
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], opened
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/lib/systemd/linger supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], ST4000VN008-2DR166, S/N:ZDH9TEX6, WWN:5-000c50-0db88f5a9, FW:SC60, 4.00 TB
Oct 24 19:36:35 localhost polkitd[1041]: Started polkitd version 0.118
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], found in smartd database: Seagate IronWolf
Oct 24 19:36:35 localhost systemd-logind[1100]: New seat seat0.
Oct 24 19:36:35 localhost systemd[1]: Started Avahi mDNS/DNS-SD Stack.
Oct 24 19:36:35 localhost avahi-daemon[1028]: Loading service file /etc/avahi/services/sftp-ssh.service.
Oct 24 19:36:35 localhost avahi-daemon[1028]: Loading service file /etc/avahi/services/ssh.service.
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event6 (Power Button)
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event5 (Power Button)
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event15 (CM Storm Keyboard -- QuickFire XT)
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event17 (CM Storm Keyboard -- QuickFire XT System Control)
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event2 (Razer Razer Abyssus V2 Keyboard)
Oct 24 19:36:35 localhost systemd-logind[1100]: Watching system buttons on /dev/input/event4 (Razer Razer Abyssus V2)
Oct 24 19:36:35 localhost systemd[1]: Started User Login Management.
Oct 24 19:36:35 localhost avahi-daemon[1028]: socket() failed: Address family not supported by protocol
Oct 24 19:36:35 localhost avahi-daemon[1028]: Failed to create IPv6 socket, proceeding in IPv4 only mode
Oct 24 19:36:35 localhost avahi-daemon[1028]: System host name is set to 'localhost'. This is not a suitable mDNS host name, looking for alternatives.
Oct 24 19:36:35 localhost avahi-daemon[1028]: socket() failed: Address family not supported by protocol
Oct 24 19:36:35 localhost avahi-daemon[1028]: Joining mDNS multicast group on interface lo.IPv4 with address 127.0.0.1.
Oct 24 19:36:35 localhost avahi-daemon[1028]: New relevant interface lo.IPv4 for mDNS.
Oct 24 19:36:35 localhost avahi-daemon[1028]: Network interface enumeration completed.
Oct 24 19:36:35 localhost avahi-daemon[1028]: Registering new address record for 127.0.0.1 on lo.IPv4.
Oct 24 19:36:35 localhost polkitd[1041]: Loading rules from directory /etc/polkit-1/rules.d
Oct 24 19:36:35 localhost polkitd[1041]: Loading rules from directory /usr/share/polkit-1/rules.d
Oct 24 19:36:35 localhost polkitd[1041]: Finished loading, compiling and executing 4 rules
Oct 24 19:36:35 localhost systemd[1]: Started Authorization Manager.
Oct 24 19:36:35 localhost polkitd[1041]: Acquired the name org.freedesktop.PolicyKit1 on the system bus
Oct 24 19:36:35 localhost systemd[1]: Starting Modem Manager...
Oct 24 19:36:35 localhost systemd[1]: Starting firewalld - dynamic firewall daemon...
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost ModemManager[1130]: <info>  ModemManager (version 1.14.8) starting in system bus...
Oct 24 19:36:35 localhost systemd[1]: Started Modem Manager.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], is SMART capable. Adding to "monitor" list.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], state read from /var/lib/smartmontools/smartd.ST4000VN008_2DR166-ZDH9TEX6.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb, type changed from 'scsi' to 'sat'
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], opened
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], Samsung SSD 860 EVO 500GB, S/N:S4CNNF0M700158E, WWN:5-002538-e4970024c, FW:RVT04B6Q, 500 GB
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], found in smartd database: Samsung based SSDs
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], can't monitor Current_Pending_Sector count - no Attribute 197
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], can't monitor Offline_Uncorrectable count - no Attribute 198
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], is SMART capable. Adding to "monitor" list.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], state read from /var/lib/smartmontools/smartd.Samsung_SSD_860_EVO_500GB-S4CNNF0M700158E.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc, type changed from 'scsi' to 'sat'
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], opened
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], Samsung SSD 860 EVO 500GB, S/N:S4XBNF0N188995Z, WWN:5-002538-ee010419c, FW:RVT04B6Q, 500 GB
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], found in smartd database: Samsung based SSDs
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], can't monitor Current_Pending_Sector count - no Attribute 197
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], can't monitor Offline_Uncorrectable count - no Attribute 198
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], is SMART capable. Adding to "monitor" list.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], state read from /var/lib/smartmontools/smartd.Samsung_SSD_860_EVO_500GB-S4XBNF0N188995Z.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, opened
Oct 24 19:36:35 localhost systemd[1]: Started firewalld - dynamic firewall daemon.
Oct 24 19:36:35 localhost systemd[1]: Reached target Preparation for Network.
Oct 24 19:36:35 localhost systemd[1]: Starting Network Manager...
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, Samsung SSD 970 EVO Plus 500GB, S/N:S4EVNX0R520351N, FW:2B2QEXM7, 500 GB
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, is SMART capable. Adding to "monitor" list.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, state read from /var/lib/smartmontools/smartd.Samsung_SSD_970_EVO_Plus_500GB-S4EVNX0R520351N.nvme.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, opened
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, Samsung SSD 970 EVO 250GB, S/N:S465NX0M120880P, FW:2B2QEXE7, 250 GB
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, is SMART capable. Adding to "monitor" list.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, state read from /var/lib/smartmontools/smartd.Samsung_SSD_970_EVO_250GB-S465NX0M120880P.nvme.state
Oct 24 19:36:35 localhost smartd[1051]: Monitoring 3 ATA/SATA, 0 SCSI/SAS and 2 NVMe devices
Oct 24 19:36:35 localhost kernel: bpfilter: Loaded bpfilter_umh pid 1140
Oct 24 19:36:35 localhost unknown: Started bpfilter
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4381] NetworkManager (version 1.32.12) is starting... (for the first time)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4382] Read config: /etc/NetworkManager/NetworkManager.conf (etc: dns.conf)
Oct 24 19:36:35 localhost systemd[1]: Started Network Manager.
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4394] bus-manager: acquired D-Bus service "org.freedesktop.NetworkManager"
Oct 24 19:36:35 localhost systemd[1]: Reached target Network.
Oct 24 19:36:35 localhost systemd[1]: Starting NTP client/server...
Oct 24 19:36:35 localhost systemd[1]: Starting CUPS Scheduler...
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4413] manager[0x561e7f900000]: monitoring kernel firmware directory '/lib/firmware'.
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.hostname1' unit='dbus-org.freedesktop.hostname1.service' requested by ':1.6' (uid=0 pid=1138 comm="/usr/sbin/NetworkManager --no-daemon ")
Oct 24 19:36:35 localhost systemd[1]: Starting OpenSSH Daemon...
Oct 24 19:36:35 localhost systemd[1]: Starting Permit User Sessions...
Oct 24 19:36:35 localhost sshd-gen-keys-start[1158]: Checking for missing server keys in /etc/ssh
Oct 24 19:36:35 localhost systemd[1]: Starting Hostname Service...
Oct 24 19:36:35 localhost systemd[1]: Finished Permit User Sessions.
Oct 24 19:36:35 localhost systemd[1]: Starting Hold until boot process finishes up...
Oct 24 19:36:35 localhost chronyd[1168]: chronyd version 4.1 starting (+CMDMON +NTP +REFCLOCK +RTC +PRIVDROP +SCFILTER +SIGND +ASYNCDNS +NTS +SECHASH +IPV6 -DEBUG)
Oct 24 19:36:35 localhost chronyd[1168]: Could not open command socket on [::1]:323
Oct 24 19:36:35 localhost chronyd[1168]: Frequency 22.660 +/- 0.223 ppm read from /var/lib/chrony/drift
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost sshd[1175]: Server listening on 0.0.0.0 port 22.
Oct 24 19:36:35 localhost systemd[1]: Started OpenSSH Daemon.
Oct 24 19:36:35 localhost systemd[1]: Started NTP client/server.
Oct 24 19:36:35 localhost systemd[1]: Reached target System Time Synchronized.
Oct 24 19:36:35 localhost systemd[1]: Started Backup of RPM database.
Oct 24 19:36:35 localhost systemd[1]: Started Backup of /etc/sysconfig.
Oct 24 19:36:35 localhost systemd[1]: Started Balance block groups on a btrfs filesystem.
Oct 24 19:36:35 localhost systemd[1]: Started Defragment file data and/or directory metadata.
Oct 24 19:36:35 localhost systemd[1]: Started Scrub btrfs filesystem, verify block checksums.
Oct 24 19:36:35 localhost systemd[1]: Started Discard unused blocks on a mounted filesystem.
Oct 24 19:36:35 localhost systemd[1]: Started Check if mainboard battery is Ok.
Oct 24 19:36:35 localhost systemd[1]: Started Discard unused blocks once a week.
Oct 24 19:36:35 localhost systemd[1]: Started Daily rotation of log files.
Oct 24 19:36:35 localhost systemd[1]: Started Daily man-db regeneration.
Oct 24 19:36:35 localhost systemd[1]: Started Logs some system statistics to the systemd journal.
Oct 24 19:36:35 localhost systemd[1]: Started Timeline of Snapper Snapshots.
Oct 24 19:36:35 localhost systemd[1]: Reached target Timer Units.
Oct 24 19:36:35 localhost systemd[1]: Starting X Display Manager...
Oct 24 19:36:35 localhost systemd[1]: Starting Temperature monitor...
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost systemd[1]: Starting Postfix Mail Transport Agent...
Oct 24 19:36:35 localhost echo[1179]: Starting mail service (Postfix)
Oct 24 19:36:35 localhost display-manager[1185]: /etc/vconsole.conf available
Oct 24 19:36:35 localhost display-manager[1185]: KEYMAP: us
Oct 24 19:36:35 localhost display-manager[1185]: Command: localectl set-keymap us
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.hostname1'
Oct 24 19:36:35 localhost systemd[1]: Started Hostname Service.
Oct 24 19:36:35 localhost display-manager[1185]: I: Using systemd /usr/share/systemd/kbd-model-map mapping
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.locale1' unit='dbus-org.freedesktop.locale1.service' requested by ':1.8' (uid=0 pid=1194 comm="localectl set-keymap us ")
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 190 Airflow_Temperature_Cel changed from 71 to 73
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 194 Temperature_Celsius changed from 29 to 27
Oct 24 19:36:35 localhost systemd[1]: Starting Locale Service...
Oct 24 19:36:35 localhost systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:36:35 localhost systemd[1]: Finished Temperature monitor.
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4832] hostname: hostname: using hostnamed
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4833] dns-mgr[0x561e7f8db230]: init: dns=dnsmasq,systemd-resolved rc-manager=netconfig, plugin=dnsmasq
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4835] manager[0x561e7f900000]: rfkill: Wi-Fi hardware radio set disabled
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4836] manager[0x561e7f900000]: rfkill: WWAN hardware radio set enabled
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.ColorManager' unit='colord.service' requested by ':1.9' (uid=0 pid=1156 comm="/usr/sbin/cupsd -l ")
Oct 24 19:36:35 localhost systemd[1]: Starting Manage, Install and Generate Color Profiles...
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4854] Loaded device plugin: NMAtmManager (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-adsl.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4870] Loaded device plugin: NMBluezManager (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-bluetooth.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4874] Loaded device plugin: NMOvsFactory (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-ovs.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4888] Loaded device plugin: NMTeamFactory (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-team.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4899] Loaded device plugin: NMWifiFactory (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-wifi.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4903] Loaded device plugin: NMWwanFactory (/usr/lib64/NetworkManager/1.32.12/libnm-device-plugin-wwan.so)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4904] manager: rfkill: Wi-Fi enabled by radio killswitch; disabled by state file
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4904] manager: rfkill: WWAN enabled by radio killswitch; enabled by state file
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4905] manager: Networking is enabled by state file
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.nm_dispatcher' unit='dbus-org.freedesktop.nm-dispatcher.service' requested by ':1.6' (uid=0 pid=1138 comm="/usr/sbin/NetworkManager --no-daemon ")
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4908] dhcp-init: Using DHCP client 'dhclient'
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4916] settings: Loaded settings plugin: keyfile (internal)
Oct 24 19:36:35 localhost systemd[1]: Starting Network Manager Script Dispatcher Service...
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4931] device (lo): carrier: link connected
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4932] manager: (lo): new Generic device (/org/freedesktop/NetworkManager/Devices/1)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4936] manager: (enp5s0): new Ethernet device (/org/freedesktop/NetworkManager/Devices/2)
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.4942] device (enp5s0): state change: unmanaged -> unavailable (reason 'managed', sys-iface-state: 'external')
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.ColorManager'
Oct 24 19:36:35 localhost systemd[1]: Started Manage, Install and Generate Color Profiles.
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.nm_dispatcher'
Oct 24 19:36:35 localhost systemd[1]: Started Network Manager Script Dispatcher Service.
Oct 24 19:36:35 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.locale1'
Oct 24 19:36:35 localhost systemd[1]: Started Locale Service.
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.5231] ovsdb: Could not connect: No such file or directory
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.5231] ovsdb: disconnected from ovsdb
Oct 24 19:36:35 localhost NetworkManager[1138]: <info>  [1635096995.5237] modem-manager: ModemManager available
Oct 24 19:36:35 localhost systemd[1]: Received SIGRTMIN+21 from PID 490 (plymouthd).
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.Accounts' unit='accounts-daemon.service' requested by ':1.13' (uid=0 pid=1243 comm="/usr/sbin/gdm ")
Oct 24 19:36:35 localhost systemd[1]: Starting Accounts Service...
Oct 24 19:36:35 localhost systemd[1]: Started CUPS Scheduler.
Oct 24 19:36:35 localhost accounts-daemon[1277]: started daemon version 0.6.55
Oct 24 19:36:35 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.Accounts'
Oct 24 19:36:35 localhost accounts-daemon[1277]: g_dbus_interface_skeleton_get_object_path: assertion 'G_IS_DBUS_INTERFACE_SKELETON (interface_)' failed
Oct 24 19:36:35 localhost systemd[1]: Started Accounts Service.
Oct 24 19:36:35 localhost systemd[1]: Created slice User Slice of UID 451.
Oct 24 19:36:35 localhost systemd[1]: Starting User Runtime Directory /run/user/451...
Oct 24 19:36:35 localhost systemd-logind[1100]: New session c1 of user gdm.
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], SMART Usage Attribute: 190 Airflow_Temperature_Cel changed from 70 to 68
Oct 24 19:36:35 localhost systemd[1]: Finished User Runtime Directory /run/user/451.
Oct 24 19:36:35 localhost systemd[1]: Starting User Manager for UID 451...
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, number of Error Log entries increased from 936 to 955
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, number of Error Log entries increased from 2295 to 2314
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sda [SAT], state written to /var/lib/smartmontools/smartd.ST4000VN008_2DR166-ZDH9TEX6.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdb [SAT], state written to /var/lib/smartmontools/smartd.Samsung_SSD_860_EVO_500GB-S4CNNF0M700158E.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/sdc [SAT], state written to /var/lib/smartmontools/smartd.Samsung_SSD_860_EVO_500GB-S4XBNF0N188995Z.ata.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme0, state written to /var/lib/smartmontools/smartd.Samsung_SSD_970_EVO_Plus_500GB-S4EVNX0R520351N.nvme.state
Oct 24 19:36:35 localhost smartd[1051]: Device: /dev/nvme1, state written to /var/lib/smartmontools/smartd.Samsung_SSD_970_EVO_250GB-S465NX0M120880P.nvme.state
Oct 24 19:36:35 localhost systemd[1]: Started Self Monitoring and Reporting Technology (SMART) Daemon.
Oct 24 19:36:35 localhost systemd[1341]: pam_unix(systemd-user:session): session opened for user gdm(uid=451) by (uid=0)
Oct 24 19:36:35 localhost postfix/postfix-script[1403]: starting the Postfix mail system
Oct 24 19:36:35 localhost postfix/master[1406]: daemon started -- version 3.6.2, configuration /etc/postfix
Oct 24 19:36:35 localhost systemd[1341]: Queued start job for default target Main User Target.
Oct 24 19:36:35 localhost systemd[1341]: Created slice User Application Slice.
Oct 24 19:36:35 localhost systemd[1341]: Started Daily Cleanup of User's Temporary Directories.
Oct 24 19:36:35 localhost systemd[1341]: Reached target Paths.
Oct 24 19:36:35 localhost systemd[1341]: Reached target Timers.
Oct 24 19:36:35 localhost systemd[1341]: Starting D-Bus User Message Bus Socket...
Oct 24 19:36:35 localhost systemd[1341]: Listening on Multimedia System.
Oct 24 19:36:35 localhost systemd[1341]: Listening on Sound System.
Oct 24 19:36:35 localhost systemd[1341]: Starting Create User's Volatile Files and Directories...
Oct 24 19:36:35 localhost systemd[1341]: Finished Create User's Volatile Files and Directories.
Oct 24 19:36:35 localhost systemd[1341]: Listening on D-Bus User Message Bus Socket.
Oct 24 19:36:35 localhost systemd[1341]: Reached target Sockets.
Oct 24 19:36:35 localhost systemd[1341]: Reached target Basic System.
Oct 24 19:36:35 localhost systemd[1341]: Reached target Main User Target.
Oct 24 19:36:35 localhost systemd[1341]: Startup finished in 82ms.
Oct 24 19:36:35 localhost systemd[1]: Started User Manager for UID 451.
Oct 24 19:36:35 localhost systemd[1]: Started Session c1 of User gdm.
Oct 24 19:36:35 localhost systemd[1]: Started Postfix Mail Transport Agent.
Oct 24 19:36:35 localhost systemd[1]: Started Command Scheduler.
Oct 24 19:36:35 localhost cron[1432]: (CRON) STARTUP (1.5.7)
Oct 24 19:36:35 localhost cron[1432]: (CRON) INFO (RANDOM_DELAY will be scaled with factor 83% if used.)
Oct 24 19:36:35 localhost cron[1432]: (CRON) INFO (running with inotify support)
Oct 24 19:36:35 localhost gdm-launch-environment][1311]: pam_unix(gdm-launch-environment:session): session opened for user gdm(uid=451) by (uid=0)
Oct 24 19:36:35 localhost systemd[1341]: Started D-Bus User Message Bus.
Oct 24 19:36:35 localhost gnome-session[1456]: gnome-session-binary[1456]: WARNING: Failed to upload environment to systemd: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-session-binary[1456]: WARNING: Failed to upload environment to systemd: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-session[1456]: gnome-session-binary[1456]: WARNING: Failed to reset failed state of units: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-session-binary[1456]: WARNING: Failed to reset failed state of units: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-session[1456]: gnome-session-binary[1456]: WARNING: Falling back to non-systemd startup procedure due to error: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-session-binary[1456]: WARNING: Falling back to non-systemd startup procedure due to error: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Name "org.freedesktop.systemd1" does not exist
Oct 24 19:36:35 localhost gnome-shell[1469]: Running GNOME Shell (using mutter 41.0) as a Wayland display server
Oct 24 19:36:35 localhost gnome-shell[1469]: Device '/dev/dri/card0' prefers shadow buffer
Oct 24 19:36:35 localhost gnome-shell[1469]: Added device '/dev/dri/card0' (amdgpu) using atomic mode setting.
Oct 24 19:36:35 localhost gnome-shell[1469]: Boot VGA GPU /dev/dri/card0 selected as primary
Oct 24 19:36:36 localhost systemd[1]: Started X Display Manager.
Oct 24 19:36:36 localhost avahi-daemon[1028]: Server startup complete. Host name is linux.local. Local service cookie is 4018900887.
Oct 24 19:36:36 localhost gnome-shell[1469]: Disabling DMA buffer screen sharing for driver 'amdgpu'.
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.a11y.Bus' requested by ':1.4' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'org.a11y.Bus'
Oct 24 19:36:36 localhost gnome-shell[1469]: Using public X11 display :1024, (using :1025 for managed services)
Oct 24 19:36:36 localhost gnome-shell[1469]: Using Wayland display name 'wayland-0'
Oct 24 19:36:36 localhost liquidctl[1035]: NZXT Kraken Z (Z53, Z63 or Z73) (experimental)
Oct 24 19:36:36 localhost liquidctl[1035]: └── Firmware version    5.7.0
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1554]: glamor: No eglstream capable devices found
Oct 24 19:36:36 localhost gnome-shell[1469]: Getting parental controls for user 451
Oct 24 19:36:36 localhost gnome-shell[1469]: Unset XDG_SESSION_ID, getCurrentSessionProxy() called outside a user session. Asking logind directly.
Oct 24 19:36:36 localhost gnome-shell[1469]: Will monitor session c1
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.freedesktop.impl.portal.PermissionStore' requested by ':1.3' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'org.freedesktop.impl.portal.PermissionStore'
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.UPower' unit='upower.service' requested by ':1.22' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost systemd[1]: Starting Daemon for power management...
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/lib/upower supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/lib/upower supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost systemd[1341]: Created slice User Core Session Slice.
Oct 24 19:36:36 localhost systemd[1341]: Starting Sound Service...
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.RealtimeKit1' unit='rtkit-daemon.service' requested by ':1.24' (uid=451 pid=1597 comm="/usr/bin/pulseaudio --daemonize=no --log-target=jo")
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.GeoClue2' unit='geoclue.service' requested by ':1.22' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost systemd[1]: Starting RealtimeKit Scheduling Policy Service...
Oct 24 19:36:36 localhost systemd[1]: Starting Location Lookup Service...
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.RealtimeKit1'
Oct 24 19:36:36 localhost systemd[1]: Started RealtimeKit Scheduling Policy Service.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully called chroot.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully dropped privileges.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully limited resources.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Canary thread running.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Running.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Watchdog thread running.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully made thread 1597 of process 1597 owned by 'gdm' high priority at nice level -12.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Supervising 1 threads of 1 processes of 1 users.
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost polkitd[1041]: Registered Authentication Agent for unix-session:c1 (system bus name :1.22 [/usr/bin/gnome-shell], object path /org/freedesktop/PolicyKit1/AuthenticationAgent, locale en_US.UTF-8)
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.gnome.Shell.Notifications' requested by ':1.3' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1544]: dbus-daemon[1544]: Activating service name='org.a11y.atspi.Registry' requested by ':1.0' (uid=451 pid=1469 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:36 localhost kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1544]: dbus-daemon[1544]: Successfully activated service 'org.a11y.atspi.Registry'
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1610]: SpiRegistry daemon is running with well-known name - org.a11y.atspi.Registry
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.UPower'
Oct 24 19:36:36 localhost systemd[1]: Started Daemon for power management.
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='fi.w1.wpa_supplicant1' unit='wpa_supplicant.service' requested by ':1.26' (uid=474 pid=1601 comm="/usr/libexec/geoclue ")
Oct 24 19:36:36 localhost systemd[1]: Starting WPA Supplicant daemon...
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Successfully activated service 'fi.w1.wpa_supplicant1'
Oct 24 19:36:36 localhost systemd[1]: Started WPA Supplicant daemon.
Oct 24 19:36:36 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.GeoClue2'
Oct 24 19:36:36 localhost systemd[1]: Started Location Lookup Service.
Oct 24 19:36:36 localhost kernel: rfkill: input handler disabled
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.freedesktop.systemd1' requested by ':1.9' (uid=451 pid=1624 comm="/usr/libexec/gsd-sharing ")
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activated service 'org.freedesktop.systemd1' failed: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:36 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:36 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:36 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:36 localhost gnome-shell[1469]: Error looking up permission: GDBus.Error:org.freedesktop.portal.Error.NotFound: No entry for geolocation
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'org.gnome.Shell.Notifications'
Oct 24 19:36:36 localhost NetworkManager[1138]: <info>  [1635096996.5788] agent-manager: agent[7a67ef5d014daa28,:1.22/org.gnome.Shell.NetworkAgent/451]: agent registered
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='ca.desrt.dconf' requested by ':1.15' (uid=451 pid=1629 comm="/usr/libexec/gsd-keyboard ")
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'ca.desrt.dconf'
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 1
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 2
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 3
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 4
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 5
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 6
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 7
Oct 24 19:36:36 localhost cpupower[1594]: Setting cpu: 8
Oct 24 19:36:36 localhost systemd[1]: my-liquidctl.service: Deactivated successfully.
Oct 24 19:36:36 localhost systemd[1]: Finished AIO startup service.
Oct 24 19:36:36 localhost gnome-session-binary[1456]: Entering running state
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.gnome.Shell.Screencast' requested by ':1.21' (uid=451 pid=1639 comm="/usr/libexec/gsd-media-keys ")
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: The XKEYBOARD keymap compiler (xkbcomp) reports:
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86BrightnessAuto
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86DisplayOff
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Info
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AspectRatio
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86DVD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Audio
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ChannelUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ChannelDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Break
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86VideoPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ZoomReset
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Editor
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86GraphicsEditor
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Presentation
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Database
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Voicemail
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Addressbook
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86DisplayToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86SpellCheck
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ContextMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MediaRepeat
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF8610ChannelsUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF8610ChannelsDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Images
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NotificationCenter
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86PickupPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86HangupPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Fn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Fn_Esc
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86FnRightShift
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric0
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric6
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric7
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric8
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric9
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericStar
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericPound
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericA
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericB
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericC
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NumericD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraFocus
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86WPSButton
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraZoomIn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraZoomOut
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraLeft
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86CameraRight
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AttendantOn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AttendantOff
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AttendantToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86LightsToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ALSToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Buttonconfig
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Taskmanager
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Journal
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86ControlPanel
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AppSelect
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Screensaver
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86VoiceCommand
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Assistant
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86BrightnessMin
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86BrightnessMax
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrev
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistNext
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrevgroup
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistNextgroup
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistAccept
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdInputAssistCancel
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86RightUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86RightDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86LeftUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86LeftDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86RootMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MediaTopMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric11
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Numeric12
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86AudioDesc
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF863DMode
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86NextFavorite
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86StopRecord
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86PauseRecord
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86VOD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Unmute
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86FastReverse
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86SlowReverse
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Data
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86OnScreenKeyboard
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86PrivacyScreenToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86SelectiveScreenshot
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro6
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro7
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro8
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro9
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro10
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro11
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro12
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro13
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro14
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro15
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro16
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro17
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro18
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro19
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro20
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro21
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro22
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro23
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro24
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro25
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro26
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro27
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro28
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro29
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86Macro30
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroRecordStart
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroRecordStop
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroPresetCycle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroPreset1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroPreset2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86MacroPreset3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdLcdMenu1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdLcdMenu2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdLcdMenu3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdLcdMenu4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: > Warning:          Could not resolve keysym XF86KbdLcdMenu5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1750]: Errors from xkbcomp are not fatal to the X server
Oct 24 19:36:36 localhost pulseaudio[1597]: Unable to load mixer: Broken pipe
Oct 24 19:36:36 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:36 localhost pulseaudio[1597]: Unable to load mixer: Broken pipe
Oct 24 19:36:36 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.gnome.ScreenSaver' requested by ':1.22' (uid=451 pid=1662 comm="/usr/libexec/gsd-power ")
Oct 24 19:36:36 localhost pulseaudio[1597]: Unable to load mixer: Broken pipe
Oct 24 19:36:36 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:36 localhost gsd-media-keys[1639]: Failed to grab accelerator for keybinding settings:playback-repeat
Oct 24 19:36:36 localhost gsd-media-keys[1639]: Failed to grab accelerator for keybinding settings:hibernate
Oct 24 19:36:36 localhost gnome-shell[1469]: ATK Bridge is disabled but a11y has already been enabled.
Oct 24 19:36:36 localhost pulseaudio[1597]: Unable to load mixer: Broken pipe
Oct 24 19:36:36 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'org.gnome.ScreenSaver'
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Supervising 1 threads of 1 processes of 1 users.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully made thread 1808 of process 1597 owned by 'gdm' RT at priority 5.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Supervising 2 threads of 1 processes of 1 users.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Supervising 2 threads of 1 processes of 1 users.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Successfully made thread 1814 of process 1597 owned by 'gdm' RT at priority 5.
Oct 24 19:36:36 localhost rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:36:36 localhost pulseaudio[1597]: Module module-bluetooth-policy not loaded.
Oct 24 19:36:36 localhost pulseaudio[1597]: Module module-bluetooth-discover not loaded.
Oct 24 19:36:36 localhost systemd[1341]: Started Sound Service.
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: The XKEYBOARD keymap compiler (xkbcomp) reports:
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Unsupported maximum keycode 708, clipping.
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: >                   X11 cannot support keycodes above 255.
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86BrightnessAuto
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86DisplayOff
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Info
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AspectRatio
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86DVD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Audio
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ChannelUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ChannelDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Break
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86VideoPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ZoomReset
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Editor
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86GraphicsEditor
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Presentation
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Database
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Voicemail
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Addressbook
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86DisplayToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86SpellCheck
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ContextMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MediaRepeat
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF8610ChannelsUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF8610ChannelsDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Images
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NotificationCenter
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86PickupPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86HangupPhone
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Fn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Fn_Esc
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86FnRightShift
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric0
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric6
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric7
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric8
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric9
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericStar
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericPound
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericA
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericB
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericC
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NumericD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraFocus
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86WPSButton
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraZoomIn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraZoomOut
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraLeft
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86CameraRight
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AttendantOn
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AttendantOff
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AttendantToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86LightsToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ALSToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Buttonconfig
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Taskmanager
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Journal
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86ControlPanel
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AppSelect
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Screensaver
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86VoiceCommand
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Assistant
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86BrightnessMin
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86BrightnessMax
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrev
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistNext
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrevgroup
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistNextgroup
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistAccept
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdInputAssistCancel
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86RightUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86RightDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86LeftUp
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86LeftDown
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86RootMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MediaTopMenu
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric11
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Numeric12
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86AudioDesc
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF863DMode
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86NextFavorite
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86StopRecord
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86PauseRecord
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86VOD
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Unmute
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86FastReverse
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86SlowReverse
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Data
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86OnScreenKeyboard
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86PrivacyScreenToggle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86SelectiveScreenshot
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro6
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro7
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro8
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro9
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro10
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro11
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro12
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro13
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro14
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro15
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro16
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro17
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro18
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro19
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro20
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro21
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro22
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro23
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro24
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro25
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro26
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro27
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro28
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro29
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86Macro30
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroRecordStart
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroRecordStop
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroPresetCycle
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroPreset1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroPreset2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86MacroPreset3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdLcdMenu1
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdLcdMenu2
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdLcdMenu3
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdLcdMenu4
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: > Warning:          Could not resolve keysym XF86KbdLcdMenu5
Oct 24 19:36:36 localhost org.gnome.Shell.desktop[1815]: Errors from xkbcomp are not fatal to the X server
Oct 24 19:36:36 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Successfully activated service 'org.gnome.Shell.Screencast'
Oct 24 19:36:36 localhost avahi-daemon[1028]: Service "linux" (/etc/avahi/services/ssh.service) successfully established.
Oct 24 19:36:36 localhost avahi-daemon[1028]: Service "linux" (/etc/avahi/services/sftp-ssh.service) successfully established.
Oct 24 19:36:37 localhost gnome-shell[1469]: Registering session with GDM
Oct 24 19:36:37 localhost systemd[1]: Received SIGRTMIN+21 from PID 490 (plymouthd).
Oct 24 19:36:37 localhost systemd[1]: Finished Hold until boot process finishes up.
Oct 24 19:36:37 localhost systemd[1]: Started Getty on tty1.
Oct 24 19:36:37 localhost systemd[1]: Reached target Login Prompts.
Oct 24 19:36:37 localhost systemd[1]: Condition check resulted in /etc/init.d/after.local Compatibility being skipped.
Oct 24 19:36:37 localhost systemd[1]: Reached target Multi-User System.
Oct 24 19:36:37 localhost systemd[1]: Reached target Graphical Interface.
Oct 24 19:36:37 localhost systemd[1]: Starting Record Runlevel Change in UTMP...
Oct 24 19:36:37 localhost systemd[1]: systemd-update-utmp-runlevel.service: Deactivated successfully.
Oct 24 19:36:37 localhost systemd[1]: Finished Record Runlevel Change in UTMP.
Oct 24 19:36:37 localhost systemd[1]: Startup finished in 8.615s (firmware) + 1.918s (loader) + 1.168s (kernel) + 1.055s (initrd) + 2.906s (userspace) = 15.664s.
Oct 24 19:36:37 localhost ModemManager[1130]: <info>  [base-manager] couldn't check support for device '/sys/devices/pci0000:00/0000:00:01.2/0000:02:00.0/0000:03:05.0/0000:05:00.0': not supported by any plugin
Oct 24 19:36:38 localhost kernel: igb 0000:05:00.0 enp5s0: igb: enp5s0 NIC Link is Up 1000 Mbps Full Duplex, Flow Control: RX
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2772] device (enp5s0): carrier: link connected
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2774] device (enp5s0): state change: unavailable -> disconnected (reason 'carrier-changed', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2778] policy: auto-activating connection 'enp5s0' (04fb4043-57b2-393f-bf75-a737978f7b5c)
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2781] device (enp5s0): Activation: starting connection 'enp5s0' (04fb4043-57b2-393f-bf75-a737978f7b5c)
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2781] device (enp5s0): state change: disconnected -> prepare (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2783] manager: NetworkManager state is now CONNECTING
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.2783] device (enp5s0): state change: prepare -> config (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3408] device (enp5s0): state change: config -> ip-config (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost avahi-daemon[1028]: Joining mDNS multicast group on interface enp5s0.IPv4 with address 192.168.0.11.
Oct 24 19:36:38 localhost avahi-daemon[1028]: New relevant interface enp5s0.IPv4 for mDNS.
Oct 24 19:36:38 localhost avahi-daemon[1028]: Registering new address record for 192.168.0.11 on enp5s0.IPv4.
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3443] device (enp5s0): state change: ip-config -> ip-check (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost kernel: NET: Registered PF_PACKET protocol family
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3451] device (enp5s0): state change: ip-check -> secondaries (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3452] device (enp5s0): state change: secondaries -> activated (reason 'none', sys-iface-state: 'managed')
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3453] manager: NetworkManager state is now CONNECTED_LOCAL
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3455] manager: NetworkManager state is now CONNECTED_SITE
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3455] policy: set 'enp5s0' (enp5s0) as default for IPv4 routing and DNS
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.3458] dnsmasq: starting /sbin/dnsmasq
Oct 24 19:36:38 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activating service name='org.freedesktop.systemd1' requested by ':1.9' (uid=451 pid=1624 comm="/usr/libexec/gsd-sharing ")
Oct 24 19:36:38 localhost /usr/libexec/gdm/gdm-wayland-session[1455]: dbus-daemon[1455]: [session uid=451 pid=1455] Activated service 'org.freedesktop.systemd1' failed: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:38 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:38 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:38 localhost gsd-sharing[1624]: Failed to StopUnit service: GDBus.Error:org.freedesktop.DBus.Error.Spawn.ChildExited: Process org.freedesktop.systemd1 exited with status 1
Oct 24 19:36:38 localhost dnsmasq[1847]: started, version 2.86 cachesize 2000
Oct 24 19:36:38 localhost dnsmasq[1847]: compile time options: IPv6 GNU-getopt DBus no-UBus i18n IDN2 DHCP DHCPv6 Lua TFTP conntrack ipset auth cryptohash DNSSEC loop-detect inotify dumpfile
Oct 24 19:36:38 localhost dnsmasq[1847]: chown of PID file /run/NetworkManager/dnsmasq.pid failed: Operation not permitted
Oct 24 19:36:38 localhost dnsmasq[1847]: DBus support enabled: connected to system bus
Oct 24 19:36:38 localhost dnsmasq[1847]: warning: no upstream servers configured
Oct 24 19:36:38 localhost dnsmasq[1847]: cleared cache
Oct 24 19:36:38 localhost nscd[1052]: 1052 ignored inotify event for `/etc/resolv.conf` (file exists)
Oct 24 19:36:38 localhost nscd[1052]: 1052 ignored inotify event for `/etc/resolv.conf` (file exists)
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.4112] device (enp5s0): Activation: successful, device activated.
Oct 24 19:36:38 localhost NetworkManager[1138]: <info>  [1635096998.4129] manager: startup complete
Oct 24 19:36:38 localhost dnsmasq[1847]: setting upstream servers from DBus
Oct 24 19:36:38 localhost dnsmasq[1847]: using nameserver 192.168.0.1#53(via enp5s0)
Oct 24 19:36:38 localhost dnsmasq[1847]: using nameserver 192.168.0.1#53 for domain 0.168.192.in-addr.arpa
Oct 24 19:36:38 localhost dnsmasq[1847]: using nameserver 192.168.0.1#53 for domain 11.0.168.192.in-addr.arpa
Oct 24 19:36:38 localhost dnsmasq[1847]: cleared cache
Oct 24 19:36:39 localhost gdm-password][1830]: gkr-pam: unable to locate daemon control file
Oct 24 19:36:39 localhost gdm-password][1830]: gkr-pam: stashed password to try later in open session
Oct 24 19:36:39 localhost systemd[1]: Created slice User Slice of UID 1000.
Oct 24 19:36:39 localhost systemd[1]: Starting User Runtime Directory /run/user/1000...
Oct 24 19:36:39 localhost systemd-logind[1100]: New session 1 of user foo.
Oct 24 19:36:39 localhost systemd[1]: Finished User Runtime Directory /run/user/1000.
Oct 24 19:36:39 localhost systemd[1]: Starting User Manager for UID 1000...
Oct 24 19:36:39 localhost systemd[1980]: pam_unix(systemd-user:session): session opened for user foo(uid=1000) by (uid=0)
Oct 24 19:36:39 localhost systemd[1980]: Queued start job for default target Main User Target.
Oct 24 19:36:39 localhost systemd[1980]: Created slice User Application Slice.
Oct 24 19:36:39 localhost gdm-password][1830]: pam_unix(gdm-password:session): session opened for user foo(uid=1000) by (uid=0)
Oct 24 19:36:39 localhost systemd[1980]: Started Daily Cleanup of User's Temporary Directories.
Oct 24 19:36:39 localhost gdm-password][1830]: gkr-pam: gnome-keyring-daemon started properly and unlocked keyring
Oct 24 19:36:39 localhost systemd[1980]: Reached target Paths.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Timers.
Oct 24 19:36:39 localhost systemd[1980]: Starting D-Bus User Message Bus Socket...
Oct 24 19:36:39 localhost systemd[1980]: Listening on Multimedia System.
Oct 24 19:36:39 localhost systemd[1980]: Listening on Sound System.
Oct 24 19:36:39 localhost systemd[1980]: Starting Create User's Volatile Files and Directories...
Oct 24 19:36:39 localhost systemd[1980]: Finished Create User's Volatile Files and Directories.
Oct 24 19:36:39 localhost systemd[1980]: Listening on D-Bus User Message Bus Socket.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Sockets.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Basic System.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Main User Target.
Oct 24 19:36:39 localhost systemd[1980]: Startup finished in 70ms.
Oct 24 19:36:39 localhost systemd[1]: Started User Manager for UID 1000.
Oct 24 19:36:39 localhost systemd[1]: Started Session 1 of User foo.
Oct 24 19:36:39 localhost kernel: rfkill: input handler enabled
Oct 24 19:36:39 localhost systemd[1980]: Started D-Bus User Message Bus.
Oct 24 19:36:39 localhost systemd[1980]: Created slice Slice /app/gnome-session-manager.
Oct 24 19:36:39 localhost systemd[1980]: Created slice User Core Session Slice.
Oct 24 19:36:39 localhost systemd[1980]: Reached target GNOME Wayland Session.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Session services which should run early before the graphical session is brought up.
Oct 24 19:36:39 localhost systemd[1980]: Reached target GNOME Shell.
Oct 24 19:36:39 localhost systemd[1980]: Starting Monitor Session leader for GNOME Session...
Oct 24 19:36:39 localhost systemd[1980]: Started Monitor Session leader for GNOME Session.
Oct 24 19:36:39 localhost systemd[1980]: Reached target Tasks to be run before GNOME Session starts.
Oct 24 19:36:39 localhost systemd[1980]: Starting GNOME Session Manager (session: gnome)...
Oct 24 19:36:39 localhost gnome-keyring-pkcs11.desktop[2035]: gnome-keyring-daemon: no process capabilities, insecure memory might get used
Oct 24 19:36:39 localhost gnome-keyring-secrets.desktop[2037]: gnome-keyring-daemon: no process capabilities, insecure memory might get used
Oct 24 19:36:39 localhost gnome-keyring-ssh.desktop[2038]: gnome-keyring-daemon: no process capabilities, insecure memory might get used
Oct 24 19:36:39 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:39 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:39 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:39 localhost gnome-keyring-ssh.desktop[2042]: SSH_AUTH_SOCK=/run/user/1000/keyring/ssh
Oct 24 19:36:39 localhost systemd[1980]: Started GNOME Session Manager (session: gnome).
Oct 24 19:36:39 localhost systemd[1980]: Reached target GNOME Session Manager is ready.
Oct 24 19:36:39 localhost systemd[1980]: Starting GNOME Shell on Wayland...
Oct 24 19:36:39 localhost systemd[1980]: Starting GNOME Shell on X11...
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Skipped due to 'exec-condition'.
Oct 24 19:36:39 localhost systemd[1980]: Condition check resulted in GNOME Shell on X11 being skipped.
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Scheduled restart job, restart counter is at 1.
Oct 24 19:36:39 localhost systemd[1980]: app-gnome-xdg\x2duser\x2ddirs-2044.scope: Couldn't move process 2044 to requested cgroup '/user.slice/user-1000.slice/user@1000.service/app.slice/app-gnome-xdg\x2duser\x2ddirs-2044.scope': No such process
Oct 24 19:36:39 localhost systemd[1980]: app-gnome-xdg\x2duser\x2ddirs-2044.scope: Failed to add PIDs to scope's control group: No such process
Oct 24 19:36:39 localhost systemd[1980]: app-gnome-xdg\x2duser\x2ddirs-2044.scope: Failed with result 'resources'.
Oct 24 19:36:39 localhost systemd[1980]: Failed to start Application launched by gnome-session-binary.
Oct 24 19:36:39 localhost systemd[1980]: Stopped GNOME Shell on X11.
Oct 24 19:36:39 localhost systemd[1980]: Starting GNOME Shell on X11...
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Skipped due to 'exec-condition'.
Oct 24 19:36:39 localhost systemd[1980]: Condition check resulted in GNOME Shell on X11 being skipped.
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Scheduled restart job, restart counter is at 2.
Oct 24 19:36:39 localhost systemd[1980]: Stopped GNOME Shell on X11.
Oct 24 19:36:39 localhost systemd[1980]: Starting GNOME Shell on X11...
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Skipped due to 'exec-condition'.
Oct 24 19:36:39 localhost systemd[1980]: Condition check resulted in GNOME Shell on X11 being skipped.
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Scheduled restart job, restart counter is at 3.
Oct 24 19:36:39 localhost systemd[1980]: Stopped GNOME Shell on X11.
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Start request repeated too quickly.
Oct 24 19:36:39 localhost systemd[1980]: org.gnome.Shell@x11.service: Skipped due to 'exec-condition'.
Oct 24 19:36:39 localhost systemd[1980]: Condition check resulted in GNOME Shell on X11 being skipped.
Oct 24 19:36:39 localhost gnome-shell[2046]: Running GNOME Shell (using mutter 41.0) as a Wayland display server
Oct 24 19:36:39 localhost gnome-shell[2046]: Device '/dev/dri/card0' prefers shadow buffer
Oct 24 19:36:39 localhost gnome-shell[2046]: Added device '/dev/dri/card0' (amdgpu) using atomic mode setting.
Oct 24 19:36:39 localhost gnome-shell[2046]: Boot VGA GPU /dev/dri/card0 selected as primary
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.Daemon' unit='gvfs-daemon.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.Daemon'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service.
Oct 24 19:36:40 localhost gnome-shell[2046]: Disabling DMA buffer screen sharing for driver 'amdgpu'.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.a11y.Bus' unit='at-spi-dbus-bus.service' requested by ':1.14' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Accessibility services bus...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.a11y.Bus'
Oct 24 19:36:40 localhost systemd[1980]: Started Accessibility services bus.
Oct 24 19:36:40 localhost gnome-shell[2046]: Using public X11 display :0, (using :1 for managed services)
Oct 24 19:36:40 localhost gnome-shell[2046]: Using Wayland display name 'wayland-0'
Oct 24 19:36:40 localhost gnome-shell[2046]: Getting parental controls for user 1000
Oct 24 19:36:40 localhost gnome-shell[2046]: Unset XDG_SESSION_ID, getCurrentSessionProxy() called outside a user session. Asking logind directly.
Oct 24 19:36:40 localhost gnome-shell[2046]: Will monitor session 1
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: brave-browser.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Evolution.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Nautilus.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Terminal.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: gnome-system-monitor.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Documents.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Music.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: com.spotify.Client.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: firefox-esr.desktop
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.impl.portal.PermissionStore' unit='xdg-permission-store.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting sandboxed app permission store...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Shell.CalendarServer' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.impl.portal.PermissionStore'
Oct 24 19:36:40 localhost systemd[1980]: Started sandboxed app permission store.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.evolution.dataserver.Sources5' unit='evolution-source-registry.service' requested by ':1.17' (uid=1000 pid=2143 comm="/usr/libexec/gnome-shell/gnome-shell-calendar-serv")
Oct 24 19:36:40 localhost systemd[1980]: Starting Evolution source registry...
Oct 24 19:36:40 localhost systemd[1980]: Starting Sound Service...
Oct 24 19:36:40 localhost gnome-shell[2046]: g_strsplit: assertion 'string != NULL' failed
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Successfully made thread 2156 of process 2156 owned by 'foo' high priority at nice level -12.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 2 users.
Oct 24 19:36:40 localhost polkitd[1041]: Registered Authentication Agent for unix-session:1 (system bus name :1.49 [/usr/bin/gnome-shell], object path /org/freedesktop/PolicyKit1/AuthenticationAgent, locale en_US.UTF-8)
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.freedesktop.Telepathy.AccountManager' requested by ':1.20' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.UDisks2VolumeMonitor' unit='gvfs-udisks2-volume-monitor.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service - disk device monitor...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.Telepathy.AccountManager'
Oct 24 19:36:40 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.UDisks2' unit='udisks2.service' requested by ':1.52' (uid=1000 pid=2163 comm="/usr/libexec/gvfs/gvfs-udisks2-volume-monitor ")
Oct 24 19:36:40 localhost systemd[1]: Starting Disk Manager...
Oct 24 19:36:40 localhost udisksd[2166]: udisks daemon version 2.9.2 starting
Oct 24 19:36:40 localhost udisksd[2166]: Can't load configuration file /etc/udisks2/udisks2.conf
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.OnlineAccounts' requested by ':1.18' (uid=1000 pid=2152 comm="/usr/libexec/evolution-data-server/evolution-sourc")
Oct 24 19:36:40 localhost dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.UDisks2'
Oct 24 19:36:40 localhost systemd[1]: Started Disk Manager.
Oct 24 19:36:40 localhost udisksd[2166]: Acquired the name org.freedesktop.UDisks2 on the system message bus
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.evolution.dataserver.Sources5'
Oct 24 19:36:40 localhost systemd[1980]: Started Evolution source registry.
Oct 24 19:36:40 localhost goa-daemon[2216]: goa-daemon version 3.40.1 starting
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Identity' requested by ':1.23' (uid=1000 pid=2216 comm="/usr/libexec/goa-daemon ")
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.OnlineAccounts'
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.UDisks2VolumeMonitor'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service - disk device monitor.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Identity'
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.AfcVolumeMonitor' unit='gvfs-afc-volume-monitor.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service - Apple File Conduit monitor...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.AfcVolumeMonitor'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service - Apple File Conduit monitor.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.MTPVolumeMonitor' unit='gvfs-mtp-volume-monitor.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service - Media Transfer Protocol monitor...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.MTPVolumeMonitor'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service - Media Transfer Protocol monitor.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.GPhoto2VolumeMonitor' unit='gvfs-gphoto2-volume-monitor.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service - digital camera monitor...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.GPhoto2VolumeMonitor'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service - digital camera monitor.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.GoaVolumeMonitor' unit='gvfs-goa-volume-monitor.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost systemd[1980]: Starting Virtual filesystem service - GNOME Online Accounts monitor...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.GoaVolumeMonitor'
Oct 24 19:36:40 localhost systemd[1980]: Started Virtual filesystem service - GNOME Online Accounts monitor.
Oct 24 19:36:40 localhost gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.evolution.dataserver.Calendar8' unit='evolution-calendar-factory.service' requested by ':1.17' (uid=1000 pid=2143 comm="/usr/libexec/gnome-shell/gnome-shell-calendar-serv")
Oct 24 19:36:40 localhost systemd[1980]: Starting Evolution calendar service...
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: gnome-control-center.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Contacts.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Documents.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Nautilus.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Calculator.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Characters.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.clocks.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Notes.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.seahorse.Application.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Photos.desktop
Oct 24 19:36:40 localhost gnome-shell[2046]: Warning: Hiding app because parental controls not yet initialised: org.gnome.Terminal.desktop
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Shell.CalendarServer'
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Shell.Notifications' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost at-spi-bus-launcher[2131]: dbus-daemon[2131]: Activating service name='org.a11y.atspi.Registry' requested by ':1.0' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:40 localhost at-spi-bus-launcher[2131]: dbus-daemon[2131]: Successfully activated service 'org.a11y.atspi.Registry'
Oct 24 19:36:40 localhost at-spi-bus-launcher[2291]: SpiRegistry daemon is running with well-known name - org.a11y.atspi.Registry
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME Shell on Wayland.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME Session is initialized.
Oct 24 19:36:40 localhost systemd[1980]: GNOME session X11 services is inactive.
Oct 24 19:36:40 localhost systemd[1980]: Dependency failed for GNOME XSettings service.
Oct 24 19:36:40 localhost systemd[1980]: org.gnome.SettingsDaemon.XSettings.service: Job org.gnome.SettingsDaemon.XSettings.service/start failed with result 'dependency'.
Oct 24 19:36:40 localhost systemd[1980]: gnome-session-x11-services-ready.target: Job gnome-session-x11-services-ready.target/verify-active failed with result 'dependency'.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME Session (session: gnome).
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME XSettings target.
Oct 24 19:36:40 localhost systemd[1980]: Starting Signal initialization done to GNOME Session Manager...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME accessibility service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME color management service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME date & time service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME maintenance of expirable data service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME keyboard configuration service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME keyboard shortcuts service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME power management service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME printer notifications service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME RFKill support service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME FreeDesktop screensaver service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME file sharing service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME smartcard service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME sound sample caching service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME USB protection service...
Oct 24 19:36:40 localhost systemd[1980]: Starting GNOME Wacom tablet support service...
Oct 24 19:36:40 localhost gnome-session-binary[2030]: Entering running state
Oct 24 19:36:40 localhost systemd[1980]: Finished Signal initialization done to GNOME Session Manager.
Oct 24 19:36:40 localhost kernel: rfkill: input handler disabled
Oct 24 19:36:40 localhost gnome-session[2030]: gnome-session-binary[2030]: GnomeDesktop-WARNING: Could not create transient scope for PID 2327: GDBus.Error:org.freedesktop.DBus.Error.UnixProcessIdUnknown: Process with ID 2327 does not exist.
Oct 24 19:36:40 localhost gnome-session-binary[2030]: GnomeDesktop-WARNING: Could not create transient scope for PID 2327: GDBus.Error:org.freedesktop.DBus.Error.UnixProcessIdUnknown: Process with ID 2327 does not exist.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME accessibility service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME RFKill support service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME maintenance of expirable data service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME FreeDesktop screensaver service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME smartcard service.
Oct 24 19:36:40 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:40 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:40 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:40 localhost systemd[1980]: Started Application launched by gnome-session-binary.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME accessibility target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME maintenance of expirable data target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME RFKill support target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME FreeDesktop screensaver target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME smartcard target.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME file sharing service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME USB protection service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME printer notifications service.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME date & time service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME date & time target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME printer notifications target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME file sharing target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME USB protection target.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ScreenSaver' requested by ':1.43' (uid=1000 pid=2343 comm="/usr/libexec/gsd-usb-protection ")
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME sound sample caching service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME sound sample caching target.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Shell.Notifications'
Oct 24 19:36:40 localhost gnome-session[2030]: gnome-session-binary[2030]: GnomeDesktop-WARNING: Could not create transient scope for PID 2344: GDBus.Error:org.freedesktop.DBus.Error.UnixProcessIdUnknown: Process with ID 2344 does not exist.
Oct 24 19:36:40 localhost gnome-session-binary[2030]: GnomeDesktop-WARNING: Could not create transient scope for PID 2344: GDBus.Error:org.freedesktop.DBus.Error.UnixProcessIdUnknown: Process with ID 2344 does not exist.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ScreenSaver'
Oct 24 19:36:40 localhost gsd-usb-protect[2343]: Failed to fetch USBGuard parameters: GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown: The name org.usbguard1 was not provided by any .service files
Oct 24 19:36:40 localhost NetworkManager[1138]: <info>  [1635097000.6809] agent-manager: agent[e8641c029be29f0d,:1.49/org.gnome.Shell.NetworkAgent/1000]: agent registered
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.evolution.dataserver.Calendar8'
Oct 24 19:36:40 localhost systemd[1980]: Started Evolution calendar service.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='ca.desrt.dconf' unit='dconf.service' requested by ':1.30' (uid=1000 pid=2283 comm="/usr/libexec/evolution-data-server/evolution-calen")
Oct 24 19:36:40 localhost systemd[1980]: Starting User preferences database...
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.evolution.dataserver.AddressBook10' unit='evolution-addressbook-factory.service' requested by ':1.30' (uid=1000 pid=2283 comm="/usr/libexec/evolution-data-server/evolution-calen")
Oct 24 19:36:40 localhost pulseaudio[2156]: Unable to load mixer: Broken pipe
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'ca.desrt.dconf'
Oct 24 19:36:40 localhost systemd[1980]: Started User preferences database.
Oct 24 19:36:40 localhost systemd[1980]: Starting Evolution address book service...
Oct 24 19:36:40 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:40 localhost pulseaudio[2156]: Unable to load mixer: Broken pipe
Oct 24 19:36:40 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:40 localhost pulseaudio[2156]: Unable to load mixer: Broken pipe
Oct 24 19:36:40 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:40 localhost pulseaudio[2156]: Unable to load mixer: Broken pipe
Oct 24 19:36:40 localhost kernel: usb 5-3: cannot get ctl value: req = 0x81, wValue = 0x100, wIndex = 0x1100, type = 1
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 2 users.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Successfully made thread 2437 of process 2156 owned by 'foo' RT at priority 5.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Supervising 5 threads of 2 processes of 2 users.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Supervising 5 threads of 2 processes of 2 users.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Successfully made thread 2438 of process 2156 owned by 'foo' RT at priority 5.
Oct 24 19:36:40 localhost rtkit-daemon[1600]: Supervising 6 threads of 2 processes of 2 users.
Oct 24 19:36:40 localhost dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.66' (uid=1000 pid=2156 comm="/usr/bin/pulseaudio --daemonize=no --log-target=jo")
Oct 24 19:36:40 localhost systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 19:36:40 localhost gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:36:40 localhost systemd[1980]: Started Sound Service.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.evolution.dataserver.AddressBook10'
Oct 24 19:36:40 localhost systemd[1980]: Started Evolution address book service.
Oct 24 19:36:40 localhost gnome-shell[2046]: Error looking up permission: GDBus.Error:org.freedesktop.portal.Error.NotFound: No entry for geolocation
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME keyboard configuration service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME keyboard configuration target.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME power management service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME power management target.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME Wacom tablet support service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME Wacom tablet support target.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME color management service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME color management target.
Oct 24 19:36:40 localhost systemd[1980]: Started GNOME keyboard shortcuts service.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME keyboard shortcuts target.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME Session.
Oct 24 19:36:40 localhost systemd[1980]: Reached target GNOME Wayland Session (session: gnome).
Oct 24 19:36:40 localhost systemd[1980]: Reached target Current graphical user session.
Oct 24 19:36:40 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Shell.Screencast' requested by ':1.47' (uid=1000 pid=2318 comm="/usr/libexec/gsd-media-keys ")
Oct 24 19:36:40 localhost gsd-media-keys[2318]: Failed to grab accelerator for keybinding settings:playback-repeat
Oct 24 19:36:40 localhost gsd-media-keys[2318]: Failed to grab accelerator for keybinding settings:hibernate
Oct 24 19:36:41 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Shell.Screencast'
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Guake not running, starting it
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Loading Gnome schema from: /usr/share/glib-2.0/schemas
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Language previously loaded from: /usr/share/locale
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Guake Terminal 3.7.0
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     VTE 0.66.0
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Gtk 3.24.30
Oct 24 19:36:41 localhost guake[2314]: gtk_widget_get_scale_factor: assertion 'GTK_IS_WIDGET (widget)' failed
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     created fresh notebook for workspace 0
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 19:36:41 localhost guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 19:36:41 localhost systemd[1980]: Started VTE child process 2549 launched by guake process 2314.
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     current workspace is 0
Oct 24 19:36:41 localhost guake[2314]: Binding 'F12' failed!
Oct 24 19:36:41 localhost guake.desktop[2314]: WARNING  can't bind show-focus key
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 19:36:41 localhost guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 19:36:41 localhost systemd[1980]: Started VTE child process 2596 launched by guake process 2314.
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 19:36:41 localhost guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 19:36:41 localhost systemd[1980]: Started VTE child process 2619 launched by guake process 2314.
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Guake tabs restored from /home/foo/.config/guake/session.json
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Guake initialized
Oct 24 19:36:41 localhost guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 19:36:41 localhost gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:36:41 localhost gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:36:42 localhost gnome-shell[2046]: GNOME Shell started at Sun Oct 24 2021 19:36:40 GMT+0200 (CEST)
Oct 24 19:36:42 localhost gnome-shell[2046]: Registering session with GDM
Oct 24 19:36:42 localhost gnome-shell[1469]: Connection to xwayland lost
Oct 24 19:36:42 localhost gdm-launch-environment][1311]: pam_unix(gdm-launch-environment:session): session closed for user gdm
Oct 24 19:36:42 localhost gdm-launch-environment][1311]: GLib-GObject: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:36:42 localhost systemd-logind[1100]: Session c1 logged out. Waiting for processes to exit.
Oct 24 19:36:42 localhost gsd-color[2307]: failed to connect to device: Failed to connect to missing device /org/freedesktop/ColorManager/devices/xrandr_Eizo_Nanao_Corporation_CG2420_39735039_gdm_451
Oct 24 19:36:42 localhost polkitd[1041]: Unregistered Authentication Agent for unix-session:c1 (system bus name :1.22, object path /org/freedesktop/PolicyKit1/AuthenticationAgent, locale en_US.UTF-8) (disconnected from bus)
Oct 24 19:36:42 localhost systemd[1]: session-c1.scope: Deactivated successfully.
Oct 24 19:36:42 localhost systemd[1]: session-c1.scope: Consumed 1.591s CPU time.
Oct 24 19:36:42 localhost systemd-logind[1100]: Removed session c1.
Oct 24 19:36:42 localhost gdm[1243]: Gdm: Child process -1439 was already dead.
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Nautilus' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost systemd[1980]: Created slice Slice /app/org.gnome.Terminal.
Oct 24 19:36:42 localhost systemd[1980]: Starting GNOME Terminal Server...
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Nautilus'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 19:36:42 localhost systemd[1980]: Started GNOME Terminal Server.
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 19:36:42 localhost nautilus[2671]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.Tracker3.Miner.Files' unit='tracker-miner-fs-3.service' requested by ':1.76' (uid=1000 pid=2671 comm="/usr/bin/nautilus --gapplication-service ")
Oct 24 19:36:42 localhost systemd[1980]: Created slice User Background Tasks Slice.
Oct 24 19:36:42 localhost systemd[1980]: Starting Tracker file system data miner...
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 19:36:42 localhost bijiben-shell-s[2702]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.Tracker3.Miner.Files'
Oct 24 19:36:42 localhost systemd[1980]: Started Tracker file system data miner.
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:36:42 localhost bijiben-shell-s[2702]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 19:36:42 localhost systemd[1980]: Started Application launched by gnome-shell.
Oct 24 19:36:42 localhost gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown: The name :1.95 was not provided by any .service files
Oct 24 19:36:42 localhost gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gtk.vfs.Metadata' unit='gvfs-metadata.service' requested by ':1.76' (uid=1000 pid=2671 comm="/usr/bin/nautilus --gapplication-service ")
Oct 24 19:36:42 localhost systemd[1980]: Starting Virtual filesystem metadata service...
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gtk.vfs.Metadata'
Oct 24 19:36:42 localhost systemd[1980]: Started Virtual filesystem metadata service.
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.Tracker3.Miner.Extract' unit='tracker-extract-3.service' requested by ':1.93' (uid=1000 pid=2810 comm="/usr/libexec/tracker-miner-fs-3 ")
Oct 24 19:36:42 localhost systemd[1980]: Starting Tracker metadata extractor...
Oct 24 19:36:42 localhost dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.Tracker3.Miner.Extract'
Oct 24 19:36:42 localhost systemd[1980]: Started Tracker metadata extractor.
Oct 24 19:36:43 localhost systemd[1980]: Started VTE child process 2922 launched by gnome-terminal-server process 2707.
Oct 24 19:36:43 localhost sudo[2950]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/zypper dup
Oct 24 19:36:43 localhost sudo[2950]: pam_unix(sudo:session): session opened for user root(uid=0) by (uid=1000)
Oct 24 19:36:43 localhost NetworkManager[1138]: <info>  [1635097003.8059] policy: set-hostname: set hostname to 'localhost.localdomain' (no hostname found)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:43 localhost.localdomain systemd-hostnamed[1162]: Hostname set to <localhost.localdomain> (transient)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring file `/etc/resolv.conf` (5)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:43 localhost.localdomain NetworkManager[1138]: <info>  [1635097003.8695] manager: NetworkManager state is now CONNECTED_GLOBAL
Oct 24 19:36:43 localhost.localdomain NetworkManager[1138]: <info>  [1635097003.8700] policy: set-hostname: set hostname to 'localhost.localdomain' (no hostname found)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring file `/etc/nsswitch.conf` (7)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring file `/etc/resolv.conf` (5)
Oct 24 19:36:43 localhost.localdomain nscd[1052]: 1052 monitoring directory `/etc` (2)
Oct 24 19:36:49 localhost.localdomain chronyd[1168]: Selected source 78.108.102.237 (2.opensuse.pool.ntp.org)
Oct 24 19:36:49 localhost.localdomain chronyd[1168]: System clock wrong by -2.192459 seconds
Oct 24 19:36:46 localhost.localdomain chronyd[1168]: System clock was stepped by -2.192459 seconds
Oct 24 19:36:47 localhost.localdomain chronyd[1168]: Selected source 195.113.144.238
Oct 24 19:36:50 localhost.localdomain systemd[1]: Stopping User Manager for UID 451...
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped target Main User Target.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopping D-Bus User Message Bus...
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopping Sound Service...
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped D-Bus User Message Bus.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped Sound Service.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Removed slice User Core Session Slice.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped target Basic System.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped target Paths.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped target Sockets.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped target Timers.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped Daily Cleanup of User's Temporary Directories.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Closed D-Bus User Message Bus Socket.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Closed Multimedia System.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Closed Sound System.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Stopped Create User's Volatile Files and Directories.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Removed slice User Application Slice.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Reached target Shutdown.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Finished Exit the Session.
Oct 24 19:36:50 localhost.localdomain systemd[1341]: Reached target Exit the Session.
Oct 24 19:36:50 localhost.localdomain systemd[1]: user@451.service: Deactivated successfully.
Oct 24 19:36:50 localhost.localdomain systemd[1]: Stopped User Manager for UID 451.
Oct 24 19:36:50 localhost.localdomain systemd[1]: Stopping User Runtime Directory /run/user/451...
Oct 24 19:36:50 localhost.localdomain systemd[1]: run-user-451.mount: Deactivated successfully.
Oct 24 19:36:50 localhost.localdomain systemd[1]: user-runtime-dir@451.service: Deactivated successfully.
Oct 24 19:36:50 localhost.localdomain systemd[1]: Stopped User Runtime Directory /run/user/451.
Oct 24 19:36:50 localhost.localdomain systemd[1]: Removed slice User Slice of UID 451.
Oct 24 19:36:50 localhost.localdomain systemd[1]: user-451.slice: Consumed 1.889s CPU time.
Oct 24 19:36:51 localhost.localdomain nscd[1052]: 1052 checking for monitored file `/etc/services': No such file or directory
Oct 24 19:36:51 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.opensuse.Snapper' unit='snapperd.service' requested by ':1.85' (uid=0 pid=3114 comm="/usr/lib/zypp/plugins/commit/snapper-zypp-plugin ")
Oct 24 19:36:51 localhost.localdomain systemd[1]: Starting DBus interface for snapper...
Oct 24 19:36:51 localhost.localdomain dbus-daemon[1029]: [system] Successfully activated service 'org.opensuse.Snapper'
Oct 24 19:36:51 localhost.localdomain systemd[1]: Started DBus interface for snapper.
Oct 24 19:36:51 localhost.localdomain systemd[1]: NetworkManager-dispatcher.service: Deactivated successfully.
Oct 24 19:36:52 localhost.localdomain org.gnome.Notes.SearchProvider[2702]: Unable to load location /home/foo/.local/share/bijiben: Error opening directory '/home/foo/.local/share/bijiben': No such file or directory
Oct 24 19:36:57 localhost.localdomain [RPM][3121]: Transaction ID 617599b9 started
Oct 24 19:36:57 localhost.localdomain [RPM][3121]: erase libgstvulkan-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3121]: install libgstvulkan-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3121]: erase libgstvulkan-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3121]: install libgstvulkan-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3121]: Transaction ID 617599b9 finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: erase libgstbasecamerabinsrc-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: install libgstbasecamerabinsrc-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: erase libgstbasecamerabinsrc-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: install libgstbasecamerabinsrc-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3124]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: erase libgstwayland-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: install libgstwayland-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: erase libgstwayland-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: install libgstwayland-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3127]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: erase libgstwebrtc-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: install libgstwebrtc-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: erase libgstwebrtc-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: install libgstwebrtc-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3130]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: erase libgstplayer-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: install libgstplayer-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: erase libgstplayer-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: install libgstplayer-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3133]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: erase libgstsctp-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: install libgstsctp-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: erase libgstsctp-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: install libgstsctp-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3136]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: erase libgsturidownloader-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: install libgsturidownloader-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: erase libgsturidownloader-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: install libgsturidownloader-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3139]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: erase libheif1-1.12.0-3.14.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: install libheif1-1.12.0-3.15.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: erase libheif1-1.12.0-3.14.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: install libheif1-1.12.0-3.15.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3142]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: erase libgstcodecparsers-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: install libgstcodecparsers-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: erase libgstcodecparsers-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: install libgstcodecparsers-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3145]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: erase libgstmpegts-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: install libgstmpegts-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: erase libgstmpegts-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: install libgstmpegts-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3148]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: erase libgstisoff-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: install libgstisoff-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: erase libgstisoff-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: install libgstisoff-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3151]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: erase libavutil56_70-4.4-9.2.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: install libavutil56_70-4.4-9.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: erase libavutil56_70-4.4-9.2.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: install libavutil56_70-4.4-9.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3154]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: erase libgstbadaudio-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: install libgstbadaudio-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: erase libgstbadaudio-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: install libgstbadaudio-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3157]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: erase libgstphotography-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: install libgstphotography-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: erase libgstphotography-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: install libgstphotography-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3160]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: erase libgstadaptivedemux-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: install libgstadaptivedemux-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: erase libgstadaptivedemux-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: install libgstadaptivedemux-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3163]: Transaction ID 617599ba finished: 0
Oct 24 19:36:58 localhost.localdomain [RPM][3166]: Transaction ID 617599ba started
Oct 24 19:36:58 localhost.localdomain [RPM][3166]: erase libgstcodecs-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:58 localhost.localdomain [RPM][3166]: install libgstcodecs-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3166]: erase libgstcodecs-1_0-0-1.18.5-5.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3166]: install libgstcodecs-1_0-0-1.18.5-5.4.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3166]: Transaction ID 617599ba finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: erase libpostproc55_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: install libpostproc55_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: erase libpostproc55_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: install libpostproc55_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3169]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: erase libswscale5_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: install libswscale5_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: erase libswscale5_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: install libswscale5_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3172]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: erase libavresample4_0-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: install libavresample4_0-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: erase libavresample4_0-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: install libavresample4_0-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3175]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: erase libswresample3_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: install libswresample3_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: erase libswresample3_9-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: install libswresample3_9-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3178]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: erase gstreamer-plugins-bad-1.18.5-5.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: install gstreamer-plugins-bad-1.18.5-5.4.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: erase gstreamer-plugins-bad-1.18.5-5.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: install gstreamer-plugins-bad-1.18.5-5.4.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3181]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: erase libavcodec58_134-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: install libavcodec58_134-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: erase libavcodec58_134-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: install libavcodec58_134-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3182]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: erase libavformat58_76-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: install libavformat58_76-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: erase libavformat58_76-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: install libavformat58_76-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3185]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: erase libavfilter7_110-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: install libavfilter7_110-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: erase libavfilter7_110-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: install libavfilter7_110-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3188]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: erase libavdevice58_13-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: install libavdevice58_13-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: erase libavdevice58_13-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: install libavdevice58_13-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3191]: Transaction ID 617599bb finished: 0
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: Transaction ID 617599bb started
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: erase ffmpeg-4-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: install ffmpeg-4-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: erase ffmpeg-4-4.4-9.2.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: install ffmpeg-4-4.4-9.3.x86_64: success
Oct 24 19:36:59 localhost.localdomain [RPM][3194]: Transaction ID 617599bb finished: 0
Oct 24 19:37:00 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:37:00 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:37:00 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:37:01 localhost.localdomain sudo[2950]: pam_unix(sudo:session): session closed for user root
Oct 24 19:37:03 localhost.localdomain dbus-daemon[1029]: [system] Failed to activate service 'org.bluez': timed out (service_start_timeout=25000ms)
Oct 24 19:37:03 localhost.localdomain pulseaudio[2156]: GetManagedObjects() failed: org.freedesktop.DBus.Error.TimedOut: Failed to activate service 'org.bluez': timed out (service_start_timeout=25000ms)
Oct 24 19:37:06 localhost.localdomain nscd[1052]: 1052 checking for monitored file `/etc/services': No such file or directory
Oct 24 19:37:08 localhost.localdomain systemd[1]: systemd-localed.service: Deactivated successfully.
Oct 24 19:37:11 localhost.localdomain systemd[1]: systemd-hostnamed.service: Deactivated successfully.
Oct 24 19:37:21 localhost.localdomain nscd[1052]: 1052 checking for monitored file `/etc/services': No such file or directory
Oct 24 19:37:25 localhost.localdomain sudo[3277]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/sync
Oct 24 19:37:25 localhost.localdomain sudo[3277]: pam_unix(sudo:session): session opened for user root(uid=0) by (uid=1000)
Oct 24 19:37:25 localhost.localdomain sudo[3277]: pam_unix(sudo:session): session closed for user root
Oct 24 19:37:34 localhost.localdomain geoclue[1601]: Service not used for 60 seconds. Shutting down..
Oct 24 19:37:34 localhost.localdomain systemd[1]: geoclue.service: Deactivated successfully.
Oct 24 19:37:37 localhost.localdomain systemd[1980]: vte-spawn-2e0a0a99-e155-4f0c-9978-4d3a1ddd8f21.scope: Consumed 5.571s CPU time.
Oct 24 19:37:46 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 19:37:46 localhost.localdomain gnome-shell[3381]: glamor: No eglstream capable devices found
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: The XKEYBOARD keymap compiler (xkbcomp) reports:
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86BrightnessAuto
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86DisplayOff
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Info
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AspectRatio
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86DVD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Audio
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ChannelUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ChannelDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Break
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86VideoPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ZoomReset
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Editor
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86GraphicsEditor
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Presentation
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Database
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Voicemail
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Addressbook
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86DisplayToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86SpellCheck
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ContextMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MediaRepeat
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF8610ChannelsUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF8610ChannelsDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Images
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NotificationCenter
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86PickupPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86HangupPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Fn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Fn_Esc
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86FnRightShift
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric0
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric6
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric7
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric8
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric9
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericStar
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericPound
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericA
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericB
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericC
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NumericD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraFocus
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86WPSButton
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraZoomIn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraZoomOut
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraLeft
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86CameraRight
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AttendantOn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AttendantOff
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AttendantToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86LightsToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ALSToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Buttonconfig
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Taskmanager
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Journal
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86ControlPanel
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AppSelect
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Screensaver
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86VoiceCommand
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Assistant
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86BrightnessMin
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86BrightnessMax
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrev
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistNext
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrevgroup
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistNextgroup
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistAccept
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdInputAssistCancel
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86RightUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86RightDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86LeftUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86LeftDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86RootMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MediaTopMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric11
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Numeric12
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86AudioDesc
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF863DMode
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86NextFavorite
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86StopRecord
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86PauseRecord
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86VOD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Unmute
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86FastReverse
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86SlowReverse
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Data
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86OnScreenKeyboard
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86PrivacyScreenToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86SelectiveScreenshot
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro6
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro7
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro8
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro9
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro10
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro11
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro12
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro13
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro14
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro15
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro16
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro17
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro18
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro19
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro20
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro21
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro22
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro23
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro24
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro25
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro26
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro27
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro28
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro29
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86Macro30
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroRecordStart
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroRecordStop
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroPresetCycle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroPreset1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroPreset2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86MacroPreset3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdLcdMenu1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdLcdMenu2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdLcdMenu3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdLcdMenu4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: > Warning:          Could not resolve keysym XF86KbdLcdMenu5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3440]: Errors from xkbcomp are not fatal to the X server
Oct 24 19:37:46 localhost.localdomain systemd[1980]: Reached target GNOME session X11 services.
Oct 24 19:37:46 localhost.localdomain systemd[1980]: Starting GNOME XSettings service...
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: The XKEYBOARD keymap compiler (xkbcomp) reports:
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Unsupported maximum keycode 708, clipping.
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: >                   X11 cannot support keycodes above 255.
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86BrightnessAuto
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86DisplayOff
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Info
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AspectRatio
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86DVD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Audio
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ChannelUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ChannelDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Break
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86VideoPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ZoomReset
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Editor
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86GraphicsEditor
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Presentation
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Database
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Voicemail
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Addressbook
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86DisplayToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86SpellCheck
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ContextMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MediaRepeat
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF8610ChannelsUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF8610ChannelsDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Images
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NotificationCenter
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86PickupPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86HangupPhone
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Fn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Fn_Esc
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86FnRightShift
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric0
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric6
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric7
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric8
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric9
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericStar
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericPound
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericA
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericB
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericC
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NumericD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraFocus
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86WPSButton
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraZoomIn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraZoomOut
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraLeft
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86CameraRight
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AttendantOn
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AttendantOff
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AttendantToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86LightsToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ALSToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Buttonconfig
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Taskmanager
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Journal
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86ControlPanel
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AppSelect
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Screensaver
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86VoiceCommand
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Assistant
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86BrightnessMin
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86BrightnessMax
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrev
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistNext
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistPrevgroup
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistNextgroup
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistAccept
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdInputAssistCancel
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86RightUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86RightDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86LeftUp
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86LeftDown
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86RootMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MediaTopMenu
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric11
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Numeric12
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86AudioDesc
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF863DMode
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86NextFavorite
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86StopRecord
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86PauseRecord
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86VOD
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Unmute
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86FastReverse
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86SlowReverse
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Data
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86OnScreenKeyboard
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86PrivacyScreenToggle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86SelectiveScreenshot
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro6
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro7
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro8
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro9
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro10
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro11
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro12
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro13
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro14
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro15
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro16
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro17
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro18
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro19
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro20
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro21
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro22
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro23
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro24
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro25
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro26
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro27
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro28
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro29
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86Macro30
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroRecordStart
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroRecordStop
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroPresetCycle
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroPreset1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroPreset2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86MacroPreset3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdLcdMenu1
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdLcdMenu2
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdLcdMenu3
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdLcdMenu4
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: > Warning:          Could not resolve keysym XF86KbdLcdMenu5
Oct 24 19:37:46 localhost.localdomain gnome-shell[3441]: Errors from xkbcomp are not fatal to the X server
Oct 24 19:37:46 localhost.localdomain systemd[1980]: Started GNOME XSettings service.
Oct 24 19:37:46 localhost.localdomain systemd[1980]: Reached target GNOME session X11 services.
Oct 24 19:37:46 localhost.localdomain gnome-shell[2046]: ATK Bridge is disabled but a11y has already been enabled.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 3 threads of 1 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 3632 of process 3341 owned by 'foo' RT at priority 10.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:48 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:48 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:37:52 localhost.localdomain chronyd[1168]: Selected source 195.113.144.201
Oct 24 19:38:00 localhost.localdomain systemd[1]: snapperd.service: Deactivated successfully.
Oct 24 19:38:00 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:38:00 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:38:00 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Nautilus' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Nautilus'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 19:38:41 localhost.localdomain nautilus[3861]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.101' (uid=1000 pid=3857 comm="/usr/libexec/gnome-contacts-search-provider ")
Oct 24 19:38:41 localhost.localdomain systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 19:38:41 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 19:38:41 localhost.localdomain bijiben-shell-s[3869]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:41 localhost.localdomain bijiben-shell-s[3869]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:38:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 19:38:41 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.UnknownMethod: Object does not exist at path “/org/gnome/seahorse/Application”
Oct 24 19:38:41 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 19:38:42 localhost.localdomain bijiben-shell-s[3869]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.Flatpak' unit='flatpak-session-helper.service' requested by ':1.140' (uid=1000 pid=4051 comm="/usr/bin/flatpak run --branch=stable --arch=x86_64")
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Starting flatpak session helper...
Oct 24 19:38:42 localhost.localdomain flatpak-session[4066]: Unable to start p11-kit server: Child process exited with code 2
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.Flatpak'
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started flatpak session helper.
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.portal.Documents' unit='xdg-document-portal.service' requested by ':1.140' (uid=1000 pid=4051 comm="/usr/bin/flatpak run --branch=stable --arch=x86_64")
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Starting flatpak document portal service...
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.portal.Documents'
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started flatpak document portal service.
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started app-flatpak-com.slack.Slack-4051.scope.
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var/cache supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var/data supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var/config supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.var/app/com.slack.Slack supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.portal.Flatpak' unit='flatpak-portal.service' requested by ':1.145' (uid=1000 pid=4086 comm="/usr/bin/xdg-dbus-proxy --args=40 ")
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Starting flatpak portal...
Oct 24 19:38:42 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.portal.Flatpak'
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started flatpak portal.
Oct 24 19:38:42 localhost.localdomain com.slack.Slack.desktop[4111]: [2 preload-host-spawn-strategy] Running: /app/bin/zypak-helper child - /app/extra/lib/slack/slack --type=zygote
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/run/ld-so-cache-dir supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain systemd[1980]: Started app-flatpak-com.slack.Slack-4159.scope.
Oct 24 19:38:42 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/var supports timestamps until 2038 (0x7fffffff)
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --simplifycfg-sink-common option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --global-isel-abort option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --amdgpu-atomic-optimizations option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --simplifycfg-sink-common option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --global-isel-abort option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --amdgpu-atomic-optimizations option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --simplifycfg-sink-common option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --global-isel-abort option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain firefox-esr.desktop[3620]: mesa: for the --amdgpu-atomic-optimizations option: may only occur zero or one times!
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Supervising 4 threads of 2 processes of 1 users.
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 4298 of process 3620 owned by 'foo' RT at priority 10.
Oct 24 19:38:42 localhost.localdomain rtkit-daemon[1600]: Supervising 5 threads of 3 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4110]: Initializing local storage instance
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: (electron) Sending uncompressed crash reports is deprecated and will be removed in a future version of Electron. Set { compress: true } to opt-in to the new behavior. Crash reports will be uploaded gzipped, which most crash reporting servers support.
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: Gtk-Message: 19:38:44.858: Failed to load module "canberra-gtk-module"
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: Gtk-Message: 19:38:44.858: Failed to load module "canberra-gtk-module"
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.875733:ERROR:bus.cc(392)] Failed to connect to the bus: Failed to connect to socket /run/dbus/system_bus_socket: No such file or directory
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.portal.Desktop' unit='xdg-desktop-portal.service' requested by ':1.149' (uid=1000 pid=4086 comm="/usr/bin/xdg-dbus-proxy --args=40 ")
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Starting Portal service...
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.impl.portal.desktop.gnome' unit='xdg-desktop-portal-gnome.service' requested by ':1.150' (uid=1000 pid=4324 comm="/usr/libexec/xdg-desktop-portal ")
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Starting Portal service (GNOME implementation)...
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.impl.portal.desktop.gnome'
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Started Portal service (GNOME implementation).
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.freedesktop.impl.portal.desktop.gtk' unit='xdg-desktop-portal-gtk.service' requested by ':1.150' (uid=1000 pid=4324 comm="/usr/libexec/xdg-desktop-portal ")
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Starting Portal service (GTK+/GNOME implementation)...
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: LaunchProcess: failed to execvp:
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: xdg-settings
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.impl.portal.desktop.gtk'
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Started Portal service (GTK+/GNOME implementation).
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.977776:ERROR:bus.cc(392)] Failed to connect to the bus: Failed to connect to socket /run/dbus/system_bus_socket: No such file or directory
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.977798:ERROR:bus.cc(392)] Failed to connect to the bus: Failed to connect to socket /run/dbus/system_bus_socket: No such file or directory
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.977811:ERROR:bus.cc(392)] Failed to connect to the bus: Failed to connect to socket /run/dbus/system_bus_socket: No such file or directory
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Started PipeWire Multimedia Service.
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Started PipeWire Media Session Manager.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 4375 of process 4375 owned by 'foo' high priority at nice level -11.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 6 threads of 4 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 4376 of process 4376 owned by 'foo' high priority at nice level -11.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 4377 of process 4376 owned by 'foo' RT at priority 20.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 4378 of process 4375 owned by 'foo' RT at priority 20.
Oct 24 19:38:44 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.994824:ERROR:browser_main_loop.cc(269)] Gtk: gtk_widget_add_accelerator: assertion 'GTK_IS_ACCEL_GROUP (accel_group)' failed
Oct 24 19:38:44 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193844.994871:ERROR:browser_main_loop.cc(269)] Gtk: gtk_widget_add_accelerator: assertion 'GTK_IS_ACCEL_GROUP (accel_group)' failed
Oct 24 19:38:44 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.freedesktop.portal.Desktop'
Oct 24 19:38:44 localhost.localdomain systemd[1980]: Started Portal service.
Oct 24 19:38:45 localhost.localdomain com.slack.Slack.desktop[4111]: libva error: vaGetDriverNameByIndex() failed with unknown libva error, driver_name = (null)
Oct 24 19:38:45 localhost.localdomain com.slack.Slack.desktop[4111]: [46:1024/193845.053126:ERROR:sandbox_linux.cc(374)] InitializeSandbox() called with multiple threads in process gpu-process.
Oct 24 19:38:45 localhost.localdomain gnome-shell[2046]: Source ID 4518 was not found when attempting to remove it
Oct 24 19:38:46 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193846.149264:ERROR:browser_main_loop.cc(269)] Gtk: gtk_widget_add_accelerator: assertion 'GTK_IS_ACCEL_GROUP (accel_group)' failed
Oct 24 19:38:46 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193846.170326:ERROR:browser_main_loop.cc(269)] Gtk: gtk_widget_add_accelerator: assertion 'GTK_IS_ACCEL_GROUP (accel_group)' failed
Oct 24 19:38:46 localhost.localdomain com.slack.Slack.desktop[4111]: [2:1024/193846.170372:ERROR:browser_main_loop.cc(269)] Gtk: gtk_widget_add_accelerator: assertion 'GTK_IS_ACCEL_GROUP (accel_group)' failed
Oct 24 19:38:54 localhost.localdomain org.gnome.Notes.SearchProvider[3869]: Unable to load location /home/foo/.local/share/bijiben: Error opening directory '/home/foo/.local/share/bijiben': No such file or directory
Oct 24 19:38:54 localhost.localdomain com.slack.Slack.desktop[4111]: Gkr-Message: 19:38:54.620: secret service operation failed: org.freedesktop.DBus.Error.ServiceUnknown
Oct 24 19:38:55 localhost.localdomain systemd[1980]: app-flatpak-com.slack.Slack-4159.scope: Consumed 4.233s CPU time.
Oct 24 19:38:55 localhost.localdomain systemd[1980]: app-flatpak-com.slack.Slack-4051.scope: Consumed 3.024s CPU time.
Oct 24 19:39:02 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:39:02 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:39:02 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:39:06 localhost.localdomain dbus-daemon[1029]: [system] Failed to activate service 'org.bluez': timed out (service_start_timeout=25000ms)
Oct 24 19:39:38 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:39:38 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:40:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:40:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:40:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:40:54 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:40:54 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:41:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:41:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:41:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:41:30 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:41:30 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:41:52 localhost.localdomain kernel: nf_conntrack: default automatic helper assignment has been turned off for security reasons and CT-based firewall rule not found. Use the iptables CT target to attach helpers instead.
Oct 24 19:42:13 localhost.localdomain systemd[1980]: Starting Cleanup of User's Temporary Files and Directories...
Oct 24 19:42:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:42:13 localhost.localdomain systemd[1980]: Finished Cleanup of User's Temporary Files and Directories.
Oct 24 19:42:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:42:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:43:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:43:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:43:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:43:17 localhost.localdomain chronyd[1168]: Selected source 195.113.144.238
Oct 24 19:43:17 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:43:17 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:44:13 localhost.localdomain systemd[1]: Starting Check if mainboard battery is Ok...
Oct 24 19:44:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:44:13 localhost.localdomain systemd[1]: check-battery.service: Deactivated successfully.
Oct 24 19:44:13 localhost.localdomain systemd[1]: Finished Check if mainboard battery is Ok.
Oct 24 19:44:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:44:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:44:54 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:44:54 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:45:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:45:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:45:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:46:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:46:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:46:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:47:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:47:13 localhost.localdomain systemd[1]: Started Daily Cleanup of Snapper Snapshots.
Oct 24 19:47:13 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.opensuse.Snapper' unit='snapperd.service' requested by ':1.151' (uid=0 pid=5090 comm="/usr/lib/snapper/systemd-helper --cleanup ")
Oct 24 19:47:13 localhost.localdomain systemd[1]: Starting DBus interface for snapper...
Oct 24 19:47:13 localhost.localdomain dbus-daemon[1029]: [system] Successfully activated service 'org.opensuse.Snapper'
Oct 24 19:47:13 localhost.localdomain systemd[1]: Started DBus interface for snapper.
Oct 24 19:47:13 localhost.localdomain systemd[1]: snapper-cleanup.service: Deactivated successfully.
Oct 24 19:47:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:47:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:47:24 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:47:24 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:48:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:48:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:48:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:48:13 localhost.localdomain systemd[1]: snapperd.service: Deactivated successfully.
Oct 24 19:48:17 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:48:17 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:48:34 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:48:34 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:49:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:49:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:49:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:50:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:50:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:50:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:50:14 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:50:14 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:50:27 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:50:27 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:50:59 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:50:59 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:51:18 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:51:18 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:51:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:51:43 localhost.localdomain systemd[1]: Starting Cleanup of Temporary Directories...
Oct 24 19:51:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:51:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:51:43 localhost.localdomain systemd[1]: systemd-tmpfiles-clean.service: Deactivated successfully.
Oct 24 19:51:43 localhost.localdomain systemd[1]: Finished Cleanup of Temporary Directories.
Oct 24 19:51:50 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:51:50 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:52:04 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:52:04 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:52:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:52:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:52:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:53:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:53:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:53:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:54:02 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:54:02 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:54:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:54:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:54:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:54:43 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:54:43 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:03 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:03 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:30 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:30 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:42 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:42 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:55:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:55:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:55:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:56:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:56:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:56:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][MessageChannel] Error: (msgtype=0x690008,name=PMessagePort::Msg___delete__) Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:25 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 19:56:47 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:56:47 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:57:42 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:57:42 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:57:42 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:57:42 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:57:42 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:58:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:58:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:58:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:59:09 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 19:59:09 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 19:59:09 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 19:59:09 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 19:59:09 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 19:59:09 localhost.localdomain gsd-media-keys[6381]: Sending 'toggle' message to Guake3
Oct 24 19:59:09 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 19:59:09 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635098349) is greater than comparison timestamp (1360017).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 19:59:09 localhost.localdomain gnome-shell[2046]: Window manager warning: W37 appears to be one of the offending windows with a timestamp of 1635098349.  Working around...
Oct 24 19:59:13 localhost.localdomain guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 19:59:13 localhost.localdomain guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 19:59:13 localhost.localdomain systemd[1980]: Started VTE child process 6433 launched by guake process 2314.
Oct 24 19:59:13 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 19:59:13 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 19:59:13 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 19:59:14 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:59:14 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 19:59:16 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 19:59:16 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:00:01 localhost.localdomain CRON[6507]: (root) CMD (run-parts /etc/cron.hourly)
Oct 24 20:00:01 localhost.localdomain CRON[6506]: (root) CMDEND (run-parts /etc/cron.hourly)
Oct 24 20:00:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:00:13 localhost.localdomain systemd[1]: Started Timeline of Snapper Snapshots.
Oct 24 20:00:13 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.opensuse.Snapper' unit='snapperd.service' requested by ':1.216' (uid=0 pid=6509 comm="/usr/lib/snapper/systemd-helper --timeline ")
Oct 24 20:00:13 localhost.localdomain systemd[1]: Starting DBus interface for snapper...
Oct 24 20:00:13 localhost.localdomain dbus-daemon[1029]: [system] Successfully activated service 'org.opensuse.Snapper'
Oct 24 20:00:13 localhost.localdomain systemd[1]: Started DBus interface for snapper.
Oct 24 20:00:13 localhost.localdomain systemd[1]: snapper-timeline.service: Deactivated successfully.
Oct 24 20:00:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:00:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:01:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:01:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:01:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:01:13 localhost.localdomain systemd[1]: snapperd.service: Deactivated successfully.
Oct 24 20:02:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:02:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:02:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:02:21 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:21 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Supervising 9 threads of 5 processes of 1 users.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 6612 of process 5986 owned by 'foo' RT at priority 10.
Oct 24 20:02:29 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:02:55 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:02:55 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:03:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:03:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:03:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:04:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:04:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:04:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:04:15 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:04:15 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:04:16 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:04:16 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:05:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:05:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:05:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:06:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:06:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:06:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 190 Airflow_Temperature_Cel changed from 73 to 72
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 194 Temperature_Celsius changed from 27 to 28
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], old test of type S not run at Sun Oct 24 03:00:00 2021 CEST, starting now.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], starting scheduled Short Self-Test.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sdb [SAT], old test of type S not run at Sun Oct 24 03:00:00 2021 CEST, starting now.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sdb [SAT], starting scheduled Short Self-Test.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sdc [SAT], SMART Usage Attribute: 190 Airflow_Temperature_Cel changed from 68 to 70
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sdc [SAT], old test of type S not run at Sun Oct 24 03:00:00 2021 CEST, starting now.
Oct 24 20:06:35 localhost.localdomain smartd[1051]: Device: /dev/sdc [SAT], starting scheduled Short Self-Test.
Oct 24 20:07:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:07:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:07:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:08:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:08:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:08:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:09:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:09:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:09:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:10:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:10:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:10:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:11:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:11:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:11:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:12:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:12:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:12:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:13:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:13:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:13:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:14:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:14:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:14:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:15:02 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:15:02 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:15:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:15:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:15:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:15:49 localhost.localdomain gnome-shell[2046]: libinput error: event15 - CM Storm Keyboard -- QuickFire XT: client bug: event processing lagging behind by 30ms, your system is too slow
Oct 24 20:15:59 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:15:59 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:16:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:16:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:16:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:16:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:16:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:17:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:17:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:17:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:18:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:18:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:18:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:18:47 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:18:47 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:19:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:19:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:19:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:20:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:20:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:20:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:20:18 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:20:18 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:20:48 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:20:48 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:21:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:21:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:21:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:22:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:22:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:22:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:22:49 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:22:49 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:23:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:23:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:23:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:24:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:24:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:24:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:25:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:25:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:25:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:26:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:26:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:26:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:26:36 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:26:36 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:27:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:27:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:27:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:28:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:28:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:28:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:29:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:29:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:29:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:30:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:30:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:30:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:31:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:31:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:31:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:31:48 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:31:48 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:31:54 localhost.localdomain gnome-shell[2046]: libinput error: event15 - CM Storm Keyboard -- QuickFire XT: client bug: event processing lagging behind by 23ms, your system is too slow
Oct 24 20:32:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:32:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:32:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:33:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:33:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:33:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:34:00 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:34:00 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 20:34:00 localhost.localdomain gsd-media-keys[8144]: Sending 'toggle' message to Guake3
Oct 24 20:34:00 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:34:02 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635100440) is greater than comparison timestamp (3452234).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 20:34:02 localhost.localdomain gnome-shell[2046]: Window manager warning: W68 appears to be one of the offending windows with a timestamp of 1635100440.  Working around...
Oct 24 20:34:03 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:03 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:04 localhost.localdomain sudo[8165]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/zypper dup
Oct 24 20:34:04 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:34:04 localhost.localdomain sudo[8165]: pam_unix(sudo:session): session opened for user root(uid=0) by foo(uid=1000)
Oct 24 20:34:04 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:04 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:34:04 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:34:06 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:34:06 localhost.localdomain guake.desktop[2314]: INFO     Hiding the terminal
Oct 24 20:34:06 localhost.localdomain gsd-media-keys[8215]: Sending 'toggle' message to Guake3
Oct 24 20:34:06 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:34:06 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 20:34:06 localhost.localdomain gsd-media-keys[8221]: Sending 'toggle' message to Guake3
Oct 24 20:34:06 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:34:11 localhost.localdomain sudo[8165]: pam_unix(sudo:session): session closed for user root
Oct 24 20:34:11 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:11 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635100446) is greater than comparison timestamp (3461682).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 20:34:11 localhost.localdomain gnome-shell[2046]: Window manager warning: W69 appears to be one of the offending windows with a timestamp of 1635100446.  Working around...
Oct 24 20:34:11 localhost.localdomain systemd[1980]: vte-spawn-7df5e613-3710-4bf1-9a97-85595db7514e.scope: Consumed 2.287s CPU time.
Oct 24 20:34:11 localhost.localdomain guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 20:34:11 localhost.localdomain guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 20:34:11 localhost.localdomain systemd[1980]: Started VTE child process 8303 launched by guake process 2314.
Oct 24 20:34:11 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:11 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:11 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:34:12 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:34:12 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:34:23 localhost.localdomain nscd[1052]: 1052 checking for monitored file `/etc/services': No such file or directory
Oct 24 20:34:38 localhost.localdomain nscd[1052]: 1052 checking for monitored file `/etc/services': No such file or directory
Oct 24 20:35:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:35:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:35:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:36:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:36:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:36:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:36:36 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 190 Airflow_Temperature_Cel changed from 72 to 71
Oct 24 20:36:36 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], SMART Usage Attribute: 194 Temperature_Celsius changed from 28 to 29
Oct 24 20:36:36 localhost.localdomain smartd[1051]: Device: /dev/sda [SAT], previous self-test completed without error
Oct 24 20:36:36 localhost.localdomain smartd[1051]: Device: /dev/sdb [SAT], previous self-test completed without error
Oct 24 20:36:36 localhost.localdomain smartd[1051]: Device: /dev/sdc [SAT], previous self-test completed without error
Oct 24 20:37:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:37:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:37:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:47 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Supervising 10 threads of 6 processes of 1 users.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 8572 of process 8054 owned by 'foo' RT at priority 10.
Oct 24 20:37:58 localhost.localdomain rtkit-daemon[1600]: Supervising 11 threads of 7 processes of 1 users.
Oct 24 20:38:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:38:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:38:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:38:48 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:39:43 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:39:43 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:39:43 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:39:49 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:39:49 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 20:39:49 localhost.localdomain gsd-media-keys[8631]: Sending 'toggle' message to Guake3
Oct 24 20:39:49 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:39:50 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635100789) is greater than comparison timestamp (3800240).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 20:39:50 localhost.localdomain gnome-shell[2046]: Window manager warning: W70 appears to be one of the offending windows with a timestamp of 1635100789.  Working around...
Oct 24 20:39:50 localhost.localdomain sudo[8640]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/zypper dup
Oct 24 20:39:50 localhost.localdomain sudo[8640]: pam_unix(sudo:session): session opened for user root(uid=0) by foo(uid=1000)
Oct 24 20:39:50 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:50 localhost.localdomain sudo[8640]: pam_unix(sudo:session): session closed for user root
Oct 24 20:39:50 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:55 localhost.localdomain sudo[8686]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/sync
Oct 24 20:39:55 localhost.localdomain sudo[8686]: pam_unix(sudo:session): session opened for user root(uid=0) by foo(uid=1000)
Oct 24 20:39:55 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:55 localhost.localdomain sudo[8686]: pam_unix(sudo:session): session closed for user root
Oct 24 20:39:55 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:58 localhost.localdomain guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 20:39:58 localhost.localdomain guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 20:39:58 localhost.localdomain systemd[1980]: Started VTE child process 8711 launched by guake process 2314.
Oct 24 20:39:58 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:59 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:59 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:39:59 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:39:59 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:40:05 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:40:05 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:40:06 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:40:06 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:40:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:40:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:40:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:40:58 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:40:58 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:41:13 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:41:13 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:41:13 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:41:19 localhost.localdomain firefox-esr.desktop[3341]: ###!!! [Parent][RunMessage] Error: Channel closing: too late to send/recv, messages will be lost
Oct 24 20:41:19 localhost.localdomain systemd[1980]: app-gnome-firefox\x2desr-3341.scope: Consumed 8min 7.793s CPU time.
Oct 24 20:41:22 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Nautilus' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:22 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Nautilus'
Oct 24 20:41:22 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.freedesktop.hostname1' unit='dbus-org.freedesktop.hostname1.service' requested by ':1.390' (uid=1000 pid=8955 comm="/usr/bin/nautilus --gapplication-service ")
Oct 24 20:41:22 localhost.localdomain systemd[1]: Starting Hostname Service...
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /run/systemd/unit-root/etc supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /run/systemd/unit-root/var/tmp supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain dbus-daemon[1029]: [system] Successfully activated service 'org.freedesktop.hostname1'
Oct 24 20:41:22 localhost.localdomain systemd[1]: Started Hostname Service.
Oct 24 20:41:22 localhost.localdomain nautilus[8955]: Called "net usershare info" but it failed: 'net usershare' returned error 255: net usershare: usershares are currently disabled
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain nautilus[8955]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:41:41 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.394' (uid=1000 pid=9011 comm="/usr/libexec/gnome-contacts-search-provider ")
Oct 24 20:41:41 localhost.localdomain systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 20:41:41 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.NoReply: Message recipient disconnected from message bus without replying
Oct 24 20:41:41 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.DiskUtility' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.DiskUtility'
Oct 24 20:41:52 localhost.localdomain systemd[1]: systemd-hostnamed.service: Deactivated successfully.
Oct 24 20:41:53 localhost.localdomain org.gnome.Notes.SearchProvider[9021]: Unable to load location /home/foo/.local/share/bijiben: Error opening directory '/home/foo/.local/share/bijiben': No such file or directory
Oct 24 20:42:00 localhost.localdomain polkit-agent-helper-1[9341]: gkr-pam: unable to locate daemon control file
Oct 24 20:42:00 localhost.localdomain polkit-agent-helper-1[9341]: gkr-pam: stashed password to try later in open session
Oct 24 20:42:00 localhost.localdomain polkitd[1041]: Operator of unix-session:1 successfully authenticated as unix-user:root to gain TEMPORARY authorization for action org.freedesktop.udisks2.filesystem-mount-system for system-bus-name::1.52 [/usr/libexec/gvfs/gvfs-udisks2-volume-monitor] (owned by unix-user:foo)
Oct 24 20:42:00 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:42:00 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:42:00 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Version 2021.8.22 external FUSE 29
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Mounted /dev/sdc3 (Read-Write, label "Decko", NTFS 3.1)
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Cmdline options: rw,nodev,nosuid,uid=1000,gid=100,windows_names,uhelper=udisks2
Oct 24 20:42:00 localhost.localdomain udisksd[2166]: Mounted /dev/sdc3 at /run/media/foo/Decko on behalf of uid 1000
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Mount options: nodev,nosuid,uhelper=udisks2,allow_other,nonempty,relatime,rw,default_permissions,fsname=/dev/sdc3,blkdev,blksize=4096
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Global ownership and permissions enforced, configuration type 7
Oct 24 20:42:00 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Shell.HotplugSniffer' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:42:00 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Shell.HotplugSniffer'
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:03 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:03 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:06 localhost.localdomain dbus-daemon[1029]: [system] Failed to activate service 'org.bluez': timed out (service_start_timeout=25000ms)
Oct 24 20:42:46 localhost.localdomain org.gnome.Nautilus[9493]: Cannot load libcuda.so.1
Oct 24 20:42:46 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:42:54 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:42:54 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 20:42:54 localhost.localdomain gsd-media-keys[9572]: Sending 'toggle' message to Guake3
Oct 24 20:42:54 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:42:55 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635100974) is greater than comparison timestamp (3985318).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 20:42:55 localhost.localdomain gnome-shell[2046]: Window manager warning: W87 appears to be one of the offending windows with a timestamp of 1635100974.  Working around...
Oct 24 20:42:56 localhost.localdomain sudo[9578]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/sync
Oct 24 20:42:56 localhost.localdomain sudo[9578]: pam_unix(sudo:session): session opened for user root(uid=0) by foo(uid=1000)
Oct 24 20:42:56 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:01 localhost.localdomain sudo[9578]: pam_unix(sudo:session): session closed for user root
Oct 24 20:43:01 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 20:43:04 localhost.localdomain guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 20:43:04 localhost.localdomain systemd[1980]: Started VTE child process 9585 launched by guake process 2314.
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:05 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:05 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:43:05 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:43:14 localhost.localdomain gnome-session-binary[2030]: Entering running state
Oct 24 20:43:18 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:43:18 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:43:18 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 20:43:23 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.247' (uid=1000 pid=9627 comm="gnome-terminal ")
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:43:23 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started VTE child process 9652 launched by gnome-terminal-server process 9634.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Nautilus' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Nautilus'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 20:43:27 localhost.localdomain nautilus[9703]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.UnknownMethod: No such interface “org.gnome.Shell.SearchProvider2” on object at path /org/gnome/seahorse/Application
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.410' (uid=1000 pid=9699 comm="/usr/libexec/gnome-contacts-search-provider ")
Oct 24 20:43:27 localhost.localdomain systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Timelines with detached actors are not supported
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.NoReply: Message recipient disconnected from message bus without replying
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 10144 of process 9914 owned by 'foo' RT at priority 10.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
```
