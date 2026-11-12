# Mustami models

On-device models used by [Mustami](https://apps.apple.com/app/mustami-quran-audio-reciters/id6807808835), an iOS app for listening to the Quran. They are published here so the app can download them on demand. Audio is processed on the phone and never uploaded.

## Recitation model (`recitation-v1`)

Used by the Recite tab, which follows a recitation from memory word by word.

| File | Size | SHA-256 |
| --- | --- | --- |
| `fastconformer-ios-v1.onnx` | 88,307,366 bytes | `3fc3cc1e722015cbf253456d2123db08de177afac90695708e6939a51805f63b` |

- **Source:** the Quran speech model by [Cyberistic/offline-quran-validation](https://github.com/Cyberistic/offline-quran-validation) (MIT), distributed through [Tilawa](https://github.com/yazinsai/tilawa) v0.2.0 as `fastconformer_full_mixed.onnx`.
- **Base model:** NVIDIA FastConformer, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **Change made:** int8 weights and zero points re-encoded as uint8 so the model runs on ONNX Runtime 1.19. Outputs are unchanged.

## Licence

The model is MIT-licensed by Cyberistic (see [LICENSE](LICENSE)), with attribution to NVIDIA under CC BY 4.0 for the FastConformer base. Thanks to Cyberistic and the Tilawa project for sharing it.
