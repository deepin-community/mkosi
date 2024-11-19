% mkosi-initrd(1)
%
%

# NAME

mkosi-initrd — Build initrds or unified kernel images for the current system
using mkosi

# SYNOPSIS

`mkosi-initrd [options…]`

# DESCRIPTION

`mkosi-initrd` is wrapper on top of `mkosi` to simplify the generation of
initrds and Unified Kernel Images for the current running system.

# OPTIONS

`--kernel-version=`
:   Kernel version where to look for the kernel modules to include. Defaults to
    the kernel version of the running system (`uname -r`).

`--format=`, `-t`
:   Output format. One of `cpio` (CPIO archive), `uki` (a unified kernel image
    with the image in the `.initrd` PE section) or `directory` (for generating
    an image directly in a local directory). Defaults to `cpio`.

`--output=`, `-o`
:   Name to use for the generated output image file or directory. Defaults
    to `initrd`.

    Note that this only specifies the output prefix, depending on the
    specific output format and compression used, the full output name might be
    `initrd.cpio.zst`.

`--output-dir=`, `-O`
:   Path to a directory where to place all generated artifacts. Defaults to the
    current working directory.

`--debug=`
:   Enable additional debugging output.

`--version`
:   Show package version.

`--help`, `-h`
:   Show brief usage information.

# SEE ALSO
`mkosi(1)`
