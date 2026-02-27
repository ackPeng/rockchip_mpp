# Rockchip MPP

Rockchip Media Process Platform (MPP) for Rockchip chips.

## Description

MPP (Media Process Platform) is the media processing platform for Rockchip chips.
It provides unified interfaces for video encoding, decoding, and processing.

## Supported Codecs

- H.264 / H.265 (AVC / HEVC)
- VP8 / VP9
- JPEG
- And more...

## Packages

This repository builds the following Debian packages:

- `librockchip-mpp6` - Shared library for MPP
- `librockchip-mpp-dev` - Development headers and libraries
- `librockchip-vpu6` - Legacy VPU compatibility library
- `rockchip-mpp-demos` - Demo and test programs

## Installation

### From Debian Repository

```bash
sudo apt update
sudo apt install librockchip-mpp6 librockchip-mpp-dev rockchip-mpp-demos
```

### From Built DEB Package

```bash
sudo dpkg -i librockchip-mpp6_*.deb
sudo dpkg -i librockchip-vpu6_*.deb
sudo dpkg -i librockchip-mpp-dev_*.deb
sudo dpkg -i rockchip-mpp-demos_*.deb
```

## Building from Source

### On x86_64 (Cross-compile for aarch64)

```bash
# Install cross-build dependencies
sudo dpkg --add-architecture arm64
sudo apt update
sudo apt install -y crossbuild-essential-arm64 binfmt-support qemu-user-static

# Build package
sudo apt install -y git-buildpackage
make deb
```

### On aarch64 (Native build)

```bash
# Install build dependencies
sudo apt install -y git-buildpackage cmake

# Build package
make deb
```

## Usage Examples

See the `rockchip-mpp-demos` package for example programs.

## Documentation

For detailed documentation, see the `doc/` directory in the source tree.

## License

See the `LICENSES/` directory for licensing information.

## Links

- Upstream: https://github.com/ackPeng/rockchip_mpp
- Rockchip: http://www.rock-chips.com

## Maintainer

This package is maintained by Radxa Computer Co., Ltd.
