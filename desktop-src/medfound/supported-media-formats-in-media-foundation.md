---
description: Questo argomento elenca i formati multimediali supportati da Microsoft Media Foundation in modalità nativa.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formati multimediali supportati in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238190"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formati multimediali supportati in Media Foundation

Questo argomento elenca i formati multimediali supportati da Microsoft Media Foundation in modalità nativa. Terze parti possono supportare formati aggiuntivi scrivendo plug-in personalizzati.

## <a name="file-containers"></a>Contenitori di file



| Formato                                           | Estensioni di file          | Origine supporti                                 | Sink di supporto                                   | Richiede                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2, .3gp, .3gp2, .3gpp | [Origine file MPEG-4](mpeg-4-file-source.md) | Sink di file 3GP                                | Windows 7                                                             |
| Advanced Streaming Format (ASF)                  | .asf, .wma, .wmv         | [Origine multimediale ASF](asf-media-source.md)     | [Sink multimediale ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Flusso di trasporto dati audio (ADTS).              | .aac, .adts              | Origine file ADTS                             | Nessuno                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Origine file AVI                              | Nessuno                                         | Windows 7                                                             |
| MP3                                              | mp3                     | [**Origine file MP3**](mp3-file-source.md)   | MP3 File Sink                                | Origine file: Windows Vista<br/> Sink di file: Windows 7<br/> |
| MPEG-4                                           | .m4a, .m4v, .mov, .mp4   | [Origine file MPEG-4](mpeg-4-file-source.md) | [**MPEG-4 File Sink**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Interscambio multimediale accessibile sincronizzato (SAMI) | .sami, .smi              | [Origine supporti SAMI](sami-media-source.md)   | Nessuno                                         | Windows Vista                                                         |
| Onda                                             | .wav                     | Origine file AVI                              | Nessuno                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codec audio



| Formato                                              | Decodificatore                                                                                                                                                          | Codificatore                                                                                                                                                          | Richiede      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-law Coding                                        | Codec ACM (Audio Compression Manager) μ-law                                                                                                                      | Nessuno                                                                                                                                                             | Windows Vista |
| Modulazione del codice ad impulso differenziale adattivo (ADPCM) | ACM ADPCM Codec                                                                                                                                                  | Nessuno                                                                                                                                                             | Windows Vista |
| Codifica audio avanzata (AAC)                         | [**Decodificatore AAC**](aac-decoder.md)                                                                                                                               | [**Codificatore AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Decodificatore MP3 multimediale**](windows-media-mp3-decoder.md)                                                                                                   | Nessuno                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | ACM GSM 6.10 Codec                                                                                                                                               | Nessuno                                                                                                                                                             | Windows Vista |
| Windows Media Audio (WMA)                           | [**Windows Decodificatore audio multimediale**](windowsmediaaudiodecoder.md)<br/> [**Windows Decodificatore vocale audio multimediale**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Codificatore audio multimediale**](windowsmediaaudioencoder.md)<br/> [**Windows Codificatore vocale audio multimediale**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fornisce wrapper per diversi codec ACM, elencati nella tabella precedente. Tuttavia, Media Foundation non supporta codec ACM arbitrari.

 

## <a name="video-codecs"></a>Codec video



| Formato                                                                                                         | Decodificatore                                                                                                                                                                  | Codificatore                                                                                                                             | Richiede      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| DV Video                                                                                                       | [**Decodificatore video DV**](dv-video-decoder.md)                                                                                                                             | Nessuno                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Decodificatore video H.264**](h-264-video-decoder.md)                                                                                                                       | [**Codificatore video H.264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (profilo di base H.264 compatibile con la modalità intestazione video breve MPEG-4 Pt2)<br/> | [**Decodificatore video MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nessuno                                                                                                                                | Windows 8     |
| Mjpeg                                                                                                          | Decodificatore MJPEG                                                                                                                                                            | Nessuno                                                                                                                                | Windows 7     |
| MPEG-4 parte 2                                                                                                  | [**Decodificatore video MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nessuno                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Decodificatore MPEG-4 V3 multimediale**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Decodificatore MPEG4 V1/V2 multimediale**](windowsmediampeg4decoder.md)<br/>         | Nessuno                                                                                                                                | Windows Vista |
| Windows Media Video (WMV)                                                                                      | [**Windows Decodificatore Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Windows Decodificatore schermo Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Windows Codificatore Media Video 9<br/> Windows Codificatore di schermo Media Video 9<br/> Windows Codificatore Video multimediale 7/8<br/> | Windows Vista |



 

> [!Note]  
> La colonna "Richiede" elenca il sistema operativo minimo necessario per l'uso di questi codec all'interno di un Media Foundation applizione. Alcuni di questi codec sono stati introdotti prima di Windows Vista come oggetti multimediali [DirectX](../directshow/directx-media-objects.md) (DMO). Se un codec supporta DMO, può essere usato con DirectShow [o](../directshow/directshow.md) Windows Media [Format SDK.](../wmformat/windows-media-format-11-sdk.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> <dt>

[Origini multimediali e sink](media-sources-and-sinks.md)
</dt> </dl>

 

 
