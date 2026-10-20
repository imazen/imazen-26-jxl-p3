# imazen-26-jxl-p3

imazen-26 is a corpus for testing image codecs and image processing.

This repository holds JPEG XL renders in sRGB and Display P3 (Adobe RGB sources converted to Display P3).
The XL images are in [imazen-xl-26](https://github.com/imazen/imazen-xl-26).
DNG sources are in imazen-xl-26 and have no rendered twins.

Lossless files preserve their PNG twins' samples. JPEG-in-JXL files retain
JPEG coefficients and reconstruct the original JPEG byte for byte.

Gain-map sources include explicit 16-bit PQ HDR twins; JPEG XL also carries
gain maps in `jhgm` boxes. See the decoding guide for HDR handling.

Version 2026.10.20: 1064 images,
1098 files, 3072829414 encoded bytes.

| branch | images | files | bytes |
|---|---:|---:|---:|
| `train` | 1064 | 1098 | 3072829414 |
| `validate` | 0 | 0 | 0 |
| `test` | 0 | 0 | 0 |

`main` contains documentation. Each data branch contains only its own bucket.
Related sources and all renditions share a bucket. Do not train or tune on
`validate` or `test`; keep both out of fitting and default selection.

```sh
git clone --branch train --single-branch --depth 1 https://github.com/imazen/imazen-26-jxl-p3.git
```

See [DECODING.md](DECODING.md) for decoder commands, colour/HDR handling and hashes.

`manifest.tsv` identifies each file, its bucket, encoded SHA-256, licence and
source provenance. The image licences differ; the Unsplash files retain the
[Unsplash License](https://unsplash.com/license), while the other files are
public domain or CC0 as specified per row. `provenance_json` preserves attribution
and source URLs. The corpus tooling's software licence does not replace these licences.

Layers: jxl-p3 (1098).

Source and validation: [imazen-26](https://github.com/imazen/imazen-26).
