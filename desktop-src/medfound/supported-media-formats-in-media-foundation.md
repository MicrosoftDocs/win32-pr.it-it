---
description: Questo argomento elenca i formati multimediali supportati da Microsoft Media Foundation in modalità nativa.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formati multimediali supportati in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320761"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formati multimediali supportati in Media Foundation

Questo argomento elenca i formati multimediali supportati da Microsoft Media Foundation in modalità nativa. Le terze parti possono supportare formati aggiuntivi scrivendo plug-in personalizzati.

## <a name="file-containers"></a>Contenitori di file



| Formato                                           | Estensioni di file          | Origine supporto                                 | Sink multimediale                                   | Richiede                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3G2,. 3GP,. 3gp2,. 3GPP | [Origine file MPEG-4](mpeg-4-file-source.md) | Sink di file 3GP                                | Windows 7                                                             |
| Formato di streaming avanzato (ASF)                  | . ASF,. WMA,. wmv         | [Origine supporto ASF](asf-media-source.md)     | [Sink multimediale ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Flusso di trasporto dati audio (ADTS).              | . AAC,. adts              | Origine file ADTS                             | nessuno                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Origine file AVI                              | nessuno                                         | Windows 7                                                             |
| MP3                                              | mp3                     | [**Origine file MP3**](mp3-file-source.md)   | Sink di file MP3                                | Origine file: Windows Vista<br/> Sink di file: Windows 7<br/> |
| MPEG-4                                           | . m4a,. m4v,. MOV,. MP4   | [Origine file MPEG-4](mpeg-4-file-source.md) | [**Sink di file MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Interscambio multimediale accessibile sincronizzato (SAMI) | . Sami,. SMI              | [Origine supporto SAMI](sami-media-source.md)   | nessuno                                         | Windows Vista                                                         |
| ONDA                                             | .wav                     | Origine file AVI                              | nessuno                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codec audio



| Formato                                              | Decodificatore                                                                                                                                                          | Codificatore                                                                                                                                                          | Richiede      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-codifica della legge                                        | Codec di Gestione compressione audio (ACM) μ-Law                                                                                                                      | nessuno                                                                                                                                                             | Windows Vista |
| Modulazione del codice Pulse differenziale adattivo (ADPCM) | Codec di ACM ADPCM                                                                                                                                                  | nessuno                                                                                                                                                             | Windows Vista |
| Codifica audio avanzata (AAC)                         | [**Decoder AAC**](aac-decoder.md)                                                                                                                               | [**Codificatore AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Decoder Windows Media MP3**](windows-media-mp3-decoder.md)                                                                                                   | nessuno                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Codec ACM GSM 6,10                                                                                                                                               | nessuno                                                                                                                                                             | Windows Vista |
| Windows Media Audio (WMA)                           | [**Decodificatore Windows Media Audio**](windowsmediaaudiodecoder.md)<br/> [**Decodificatore Voice Windows Media Audio**](windowsmediaaudiovoicedecoder.md)<br/> | [**Codificatore Windows Media Audio**](windowsmediaaudioencoder.md)<br/> [**Codificatore Voice Windows Media Audio**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fornisce wrapper per diversi codec ACM, elencati nella tabella precedente. Tuttavia, Media Foundation non supporta i codec ACM arbitrari.

 

## <a name="video-codecs"></a>Codec video



| Formato                                                                                                         | Decodificatore                                                                                                                                                                  | Codificatore                                                                                                                             | Richiede      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Video DV                                                                                                       | [**Decoder video DV**](dv-video-decoder.md)                                                                                                                             | nessuno                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Decoder video H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Codificatore video H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Profilo di base H. 264 compatibile con la modalità di intestazione video breve MPEG-4 PT2)<br/> | [**MPEG-4 Part 2 video decoder**](mpeg4part2videodecoder.md)                                                                                                            | nessuno                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Decodificatore MJPEG                                                                                                                                                            | nessuno                                                                                                                                | Windows 7     |
| MPEG-4 parte 2                                                                                                  | [**MPEG-4 Part 2 video decoder**](mpeg4part2videodecoder.md)                                                                                                            | nessuno                                                                                                                                | Windows 7     |
| MPEG-4 V1/V2/V3                                                                                                | [**Decodificatore Windows Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Decoder Windows Media MPEG4 v1/v2**](windowsmediampeg4decoder.md)<br/>         | nessuno                                                                                                                                | Windows Vista |
| Windows Media Video (WMV)                                                                                      | [**Decodificatore Windows Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Decodificatore dello schermo Windows Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Codificatore Windows Media Video 9<br/> Codificatore dello schermo Windows Media Video 9<br/> Codificatore Windows Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> La colonna "requires" elenca il sistema operativo minimo necessario per usare questi codec all'interno di un'applicazione Media Foundation. Alcuni di questi codec sono stati introdotti prima di Windows Vista come [DirectX Media Objects](../directshow/directx-media-objects.md) (DMOS). Se un codec supporta la funzionalità DMO, può essere usato con [DirectShow](../directshow/directshow.md) o con [Windows Media Format SDK](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Origini e sink multimediali](media-sources-and-sinks.md)
</dt> </dl>

 

 
