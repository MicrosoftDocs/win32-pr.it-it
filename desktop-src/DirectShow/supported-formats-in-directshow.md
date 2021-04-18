---
description: Formati supportati in DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formati supportati in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315527"
---
# <a name="supported-formats-in-directshow"></a>Formati supportati in DirectShow

DirectShow è un'architettura aperta, che significa che può supportare qualsiasi formato purché siano presenti filtri per l'analisi e la decodifica. I filtri forniti da Microsoft, come ridistribuibili tramite DirectShow o come componenti del sistema operativo Windows, offrono il supporto predefinito per i formati di file e di compressione seguenti.

Tipi di file:



| Tipo di file                                                                                        | Altre informazioni                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ASF (Advanced Systems Format), tra cui Windows Media Audio (WMA) e Windows Media Video (WMV) | [Filtro di lettura ASF WM](about-the-wm-asf-reader-filter.md)<br/> [Filtro writer ASF WM](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [Filtro Mux AVI](avi-mux-filter.md)<br/> [Filtro separatore AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtro del parser MIDI](midi-parser-filter.md)<br/> [**Filtro renderer MIDI**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |



 

Formati di compressione:



| Formato                                        | Altre informazioni                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Decoder audio Microsoft MPEG-1/gg/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Video digitale (DV)                            | [Filtro decodificatore video DV](dv-video-decoder-filter.md)<br/> [Filtro codificatore video DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Decoder video Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-4 video versione 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 versione 3                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [Filtro compressione MJPEG](mjpeg-compressor-filter.md)<br/> [Filtro di decompressione MJPEG](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG Audio Layer-3 (MP3) (solo decompressione) |                                                                                                                                                                                                                                                 |
| Audio MPEG-1 Layer I e Layer II             | [**Decoder audio Microsoft MPEG-1/gg/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtro decodificatore MPEG-1 audio](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Video MPEG-1                                  | [Filtro decodificatore video MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Decoder video Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Audio MPEG-2                                  | [**Codificatore audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Codificatore Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Video MPEG-2                                  | [**Codificatore Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/> [**Decoder video Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/> [**Codificatore video Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Per informazioni sulla disponibilità di specifici codec di terze parti per la ridistribuzione con le applicazioni DirectShow, contattare il produttore del codec.

 

 




