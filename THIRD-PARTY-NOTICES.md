# Third-party notices and license ledger

Diarist is internal software. Every dependency is free for commercial use and runs locally.
Copyleft components are used only as separate processes, and each has a permissive alternative noted.

| Component | License | Commercial use | How it's used | Alternative if distributed commercially |
|---|---|---|---|---|
| Whisper large-v3 weights | MIT | Yes | Downloaded model (`ggml-large-v3.bin`) | — |
| whisper.cpp / Whisper.net 1.9.1 | MIT | Yes | NuGet and native DLLs | — |
| ONNX Runtime GPU 1.30.0 | MIT | Yes | NuGet and native DLLs | — |
| System.Numerics.Tensors 10.0.12 | MIT | Yes | NuGet (Core) | — |
| System.CommandLine 2.0.12 | MIT | Yes | NuGet (CLI) | — |
| NUnit, NUnit3TestAdapter, NUnit.Analyzers, Microsoft.NET.Test.Sdk | MIT | Yes | Test-only | — |
| Avalonia, Avalonia.Desktop, Avalonia.Themes.Fluent 11.3.22 | MIT | Yes | NuGet (App, `DiaristApp.exe`); transitive SkiaSharp and HarfBuzzSharp (MIT) and ANGLE (BSD-3, `av_libglesv2.dll`) | — |
| Avalonia.Headless.NUnit 11.3.22 | MIT | Yes | Test-only (App tests) | — |
| CommunityToolkit.Mvvm 8.4.2 | MIT | Yes | NuGet (App): source generators plus a small runtime library | — |
| Fluent UI System Icons (path data) | MIT | Yes | Geometries copied into `src/Diarist.App/Assets/Icons.axaml` by `tools/icons/fetch_icons.py`; license below | — |
| Segoe UI Variable, Cascadia Mono | Shipped with Windows (Cascadia: SIL OFL 1.1) | Yes | Used from the system; not redistributed | — |
| pyannote community-1 (segmentation, embedding, PLDA) | CC-BY-4.0 | Yes, with credit | Converted ONNX plus arrays (Milestone 3) | — (credit below) |
| pyannote.audio (export tool only) | MIT | Yes | Dev-time Python | — |
| WeSpeaker ResNet34 embedding (inside community-1) | CC-BY-4.0 (VoxCeleb) | Yes, with credit | Converted ONNX | — |
| pyannote.audio `sample.wav` (test fixture audio) | MIT (shipped in the pyannote.audio package) | Yes | `tests/fixtures/golden` only | — |
| Silero VAD | MIT | Yes | ONNX model (Milestone 2) | — |
| ffmpeg 9.0.2 (gyan.dev "essentials" build) | GPL | Yes, internal use | Separate process; not linked. Downloaded on first use from the builder's GitHub release (`GyanD/codexffmpeg`), SHA-256-pinned; not rehosted by us (D25) | BtbN's LGPL builds (pruned over time, so they'd need rehosting), or Windows Media Foundation's AAC decoder |
| CUDA 13 runtime (cudart), cuBLAS, cuBLASLt | NVIDIA CUDA Toolkit EULA | Yes | Redistributed unmodified in the Diarist CUDA pack (`diarist-cuda13-win-x64.zip`), as the EULA's redistributable files (Attachment A) shipped with our application (D25) | — |
| cuDNN 9 | NVIDIA cuDNN license (SLA) | Yes | Redistributed unmodified in the same CUDA pack, as permitted for applications that use it | — |
| Microsoft Visual C++ 2015–2022 runtime | Microsoft redistributable | Yes | Not shipped: most systems have it; diarist stops with a link to Microsoft's installer when it is missing | App-local copies of the redist DLLs |
| Rejected: DiariZen weights | CC BY-NC 4.0 | No | Not used | — |
| Rejected: pyannoteAI precision-2 | Paid cloud API | No (not local) | Not used | — |

AAC decoding can involve patent licensing if Diarist is ever distributed commercially; Media Foundation's system decoder
covers that case.

## Credits required by CC-BY-4.0

Speaker diarization models © pyannote (Hervé Bredin and contributors), "speaker-diarization-community-1",
licensed CC-BY-4.0. The ONNX conversion was made by the Diarist project.
PLDA model trained by the BUT Speech@FIT group. Speaker embedding model from WeSpeaker (Wang et al., ICASSP 2023),
trained on VoxCeleb (CC-BY-4.0).

## Fluent UI System Icons (MIT)

Copyright (c) 2020 Microsoft Corporation.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
