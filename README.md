# Texture compressor

CLI tool for texture compression using ASTC, ETC, PVRTC and S3TC in DDS or PVR containers.

## Texture tester

A texture tester is available on https://timvanscherpenzeel.github.io/texture-compressor/.

## Status

	Work in progress

## Flags

### Required
	-c, --compression ['astc', 'etc1', 'etc2', 'pvrtc1', 'dxt1', 'dxt3', 'dxt5'] [required]
	-i, --input [example: ./docs/example.png] [required]
	-o, --output [example: ./docs/example.dds] [required]
	-m, --method ['astc', 'etc', 'pvr', 's3tc'] [required]

### Optional
	-b, --bitrate [2.0 - 4.0, default: 2.0] [not required]
	-q, --quality [0 - 10, default: 5] [not required]
	-t, --transparant [true / false, default: false] [not required]

### Tool flags
	-f, --flags ["flag value" "flag value"] [not required]

## Example

### ASTC
	node ./bin/texture-compressor.js -i ./docs/example.png -o ./docs/example-astc.dds -m astc -c astc

### ETC
	node ./bin/texture-compressor.js -i ./docs/example.png -o ./docs/example-etc1.dds -m etc -c etc1

### PVR
	node ./bin/texture-compressor.js -i ./docs/example.png -o ./docs/example-pvrtc1.pvr -m pvr -c pvrtc1

### S3TC
    node ./bin/texture-compressor.js -i ./docs/example.png -o ./docs/example-dxt5.dds -m s3tc -c dxt5

## Licence

My work is released under [GNU General Public License v3.0](https://raw.githubusercontent.com/TimvanScherpenzeel/texture-compressor/master/LICENSE).

This repository distributes multiple binary tools for Windows, Mac and Linux.

[astcenc](https://raw.githubusercontent.com/ARM-software/astc-encoder/master/license.txt)

[crunch](https://raw.githubusercontent.com/Unvanquished/crunch/master/license.txt)

[EtcTool](https://raw.githubusercontent.com/google/etc2comp/master/LICENSE)

[PVRTexToolCLI](https://community.imgtec.com/developers/powervr/sdk-end-user-licence-agreement/)
