# diarist-assets

Download host for [Diarist](https://github.com/DJGosnell) — a local, diarized, uncertainty-aware transcriber for
Windows. Diarist downloads these files on first run and checks each one's SHA-256 against its manifest; you don't need
to download anything here by hand.

The files are attached to this repository's **Releases** (tag `assets-v1`), not committed to it:

| File | Bytes | SHA-256 |
|---|---|---|
| `diarist-cuda13-win-x64.zip` | 759,376,053 | `d381e8f18c4a6ddb43d1f64126ca90f9e3950e248d4cc4c124d8b35cfd8617a9` |
| `segmentation.onnx` | 5,916,314 | `59357c1ab22429829098f711f417431b8770b2b410f87901c955e74cd52e8d47` |
| `embedding.onnx` | 26,548,732 | `badc86ab12f895f317e240294ef8b47bd35e5fc12bcf532d9fc50c2cf582a5f5` |
| `diarization.zip` | 187,139 | `45dd1762978a76d9441ba71b8acd568840fa93ae3205c39e531816075ebbee23` |

Base URL for Diarist's manifest: `https://github.com/DJGosnell/diarist-assets/releases/download/assets-v1`

## Licenses

- `diarist-cuda13-win-x64.zip`: NVIDIA CUDA runtime (cudart), cuBLAS/cuBLASLt and cuDNN 9, redistributed unmodified
  with the Diarist application under NVIDIA's CUDA Toolkit EULA (redistributable files, Attachment A) and the cuDNN
  license. These files are provided only for use with Diarist.
- `segmentation.onnx`, `embedding.onnx`, `diarization.zip`: converted from pyannote "speaker-diarization-community-1"
  © pyannote (Hervé Bredin and contributors), licensed CC-BY-4.0. PLDA model by the BUT Speech@FIT group; speaker
  embedding model from WeSpeaker (Wang et al., ICASSP 2023), trained on VoxCeleb (CC-BY-4.0). ONNX conversion by the
  Diarist project.

See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) for the full list.
