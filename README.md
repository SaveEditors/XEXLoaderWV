# X360 XEX Loader for Ghidra by Warranty Voider

This is a Ghidra loader extension for Xbox 360 XEX files.

## SaveEditors Fork Updates

This fork carries maintained fixes and publishes ready-to-install release zips.

- SaveEditors fork release: `13.0.0` (`Bug fixes`)
- Fixed PDB enum imports so enums use their actual underlying storage size instead of always importing as 8-byte enums.
- Fixed PDB root stream page counting so PDBs with sub-page root directories parse correctly.
- Fixed CodeView `LF_ARRAY` imports so byte lengths are converted into the correct element counts.
- Fixed `.pdata` handling so imported entries become real Ghidra functions instead of label-only symbols.
- Release zips for the fork are published on the [Releases](https://github.com/SaveEditors/XEXLoaderWV/releases) page.
- The upstream patch was submitted as [zeroKilo/XEXLoaderWV#33](https://github.com/zeroKilo/XEXLoaderWV/pull/33).

## Features

- Supports PDB/XDB files.
  - In the loader import page, click Advanced.
  - Tick `Load PDB File` and `Use experimental PDB loader`, then untick `Process .pdata`.
  - Select `MSDIA` parser.
- Supports XEXP delta patches.

Requires JDK 17 or newer.

[![Alt text](https://img.youtube.com/vi/coGz0f7hHTM/0.jpg)](https://www.youtube.com/watch?v=coGz0f7hHTM)

<!-- this video is outdated -->
<!-- [![Alt text](https://img.youtube.com/vi/dBoofGgraKM/0.jpg)](https://www.youtube.com/watch?v=dBoofGgraKM) -->

## Build problem with gradle wrapper

EDIT:2025.04.05

it seems you have to update

```(Ghidra Install Dir)\Ghidra\application.properties```

and upgrade the gradle version like this

```application.gradle.min=8.10```

if you have problems with building from source in eclipse with the gradle wrapper.
