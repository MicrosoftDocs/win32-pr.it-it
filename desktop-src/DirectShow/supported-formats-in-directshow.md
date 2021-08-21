---
description: Formati supportati in DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formati supportati in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e42079f29ce89ba66fcd0c03a6520769a91538eb1a9b8901115b6895420d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633231"
---
# <a name="supported-formats-in-directshow"></a>Formati supportati in DirectShow

DirectShow è un'architettura aperta, il che significa che può supportare qualsiasi formato purché siano presenti filtri per analizzarlo e decodificarlo. I filtri forniti da Microsoft, come ridistribuibili tramite DirectShow o come componenti del sistema operativo Windows, forniscono il supporto predefinito per i seguenti formati di file e compressione.

Tipi di file:



| Tipo di file                                                                                        | Altre informazioni                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF), tra cui Windows Media Audio (WMA) e Windows Media Video (WMV) | [Filtro lettore ASF WM](about-the-wm-asf-reader-filter.md)<br/> [Filtro di WM ASF Writer](wm-asf-writer-filter.md)<br/> |
| Aiff                                                                                             | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [Filtro Mux AVI](avi-mux-filter.md)<br/> [Filtro separatore AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtro parser MIDI](midi-parser-filter.md)<br/> [**Filtro del renderer MIDI**](midi-renderer-filter.md)<br/>           |
| Snd                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtro del parser WAVE](wave-parser-filter.md)                                                                                      |



 

Formati di compressione:



| Formato                                        | Altre informazioni                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Decodificatore audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Video digitale (DV)                            | [Filtro del decodificatore video DV](dv-video-decoder-filter.md)<br/> [Filtro codificatore video DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Microsoft MPEG-2 Video Decoder**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| Video ISO MPEG-4 versione 1.0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 versione 3                    |                                                                                                                                                                                                                                                 |
| Mjpeg                                         | [Filtro MJPEG Filter](mjpeg-compressor-filter.md)<br/> [Filtro decompressore MJPEG](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG Audio Layer-3 (MP3) (solo decompressione) |                                                                                                                                                                                                                                                 |
| Audio MPEG-1 di livello I e di livello II             | [**Decodificatore audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtro decodificatore audio MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Video MPEG-1                                  | [Filtro del decodificatore video MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Microsoft MPEG-2 Video Decoder**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Audio MPEG-2                                  | [**Microsoft MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Codificatore Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Video MPEG-2                                  | [**Codificatore Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/> [**Microsoft MPEG-2 Video Decoder**](microsoft-mpeg-2-video-decoder.md)<br/> [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Per informazioni sulla disponibilità di codec di terze parti specifici per la ridistribuzione con DirectShow applicazioni, contattare il produttore del codec.

 

 




