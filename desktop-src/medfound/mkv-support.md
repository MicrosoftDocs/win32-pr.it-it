---
description: Questa sezione descrive il supporto Media Foundation per i file di Matroska Media Container (MKV).
title: Supporto di Matroska Media Container (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb7a836b4a0409af3c359c8d81a0f232e6eb61082960cfb2b0705531de199c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102141"
---
# <a name="matroska-media-container-mkv-support"></a>Supporto di Matroska Media Container (MKV)

Questa sezione descrive il supporto Media Foundation per i file di Matroska Media Container (MKV).

Il formato MKV può supportare più codec video e audio, ad esempio audio H.264 e AAC. In generale, i contenitori descrivono come vengono disposti i dati audio e video e quali informazioni supplementari vengono usate per descrivere tali flussi A/V. I contenitori possono anche includere dati che integrano flussi A/V, ad esempio titolo, lingue dei flussi audio, tracce di sottotitoli o sottotitoli, tipi di carattere per tali sottotitoli, immagini, informazioni sui capitoli e menu. MKV è un formato altamente flessibile che supporta molte di queste funzionalità del contenitore. Per altre informazioni sul formato MKV, vedere [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Supporto delle funzionalità dei contenitori MKV
Le funzionalità del contenitore MKV sono supportate in Media Foundation nei modi seguenti:
- Se sono presenti una o più tracce video, verrà riprodotta la prima traccia.
- Se sono presenti una o più tracce audio, verrà riprodotta la prima traccia.
- Le tracce didascalia sono supportate, ma non sono selezionate (riprodotte) per impostazione predefinita.
- Se sono presenti uno o più tipi di carattere o immagini, non verrà eseguito il rendering di didascalie e immagini, anche se il file verrà caricato e riprodotto.
- Le informazioni sul menu non sono supportate e non verranno visualizzate, ma il file verrà caricato e riprodotto.
- Se i file con capitoli fanno riferimento a file supplementari, i file supplementari non verranno riprodotti.
- Le immagini di anteprima sono disponibili quando si esplorano i file nelle unità USB usando il browser di file.

Questo set di funzionalità deve consentire la riproduzione della maggior parte dei file MKV se contengono codec supportati.
Sono supportati i file MKV che contengono tracce video e audio codificate con i codec elencati nella sezione seguente.

## <a name="supported-mkv-codecs"></a>Codec MKV supportati

### <a name="video-codec-support-for-mkv"></a>Supporto di codec video per MKV

ID Matroska: V_MPEG4/ISO/AVC

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264
- Descrizione: video H.264
- Identificatori FourCC o WAV: H264

ID Matroska: V_MPEG2

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2
- Descrizione: video MPEG-2

ID Matroska: V_MPEG1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1
- Descrizione: video MPEG-1
- Identificatori FourCC o WAV: MPG1

ID Matroska: V_MPEG4/MS/V3

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43
- Descrizione: codec Microsoft MPEG 4 versione 3
- Identificatori FourCC o WAV: MP43

ID Matroska: V_MPEG4/ISO/ASP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrizione: video MPEG-4 parte 2
- Identificatori FourCC o WAV: MP4V

ID Matroska: V_MS/VFW/FOURCC

- Descrizione: Mappe a diversi codec in genere supportati nel formato AVI disponibili nella console.

ID Matroska: V_THEORA

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora
- Descrizione: Theora
- Identificatori FourCC o WAV: theo

ID Matroska: V_MPEG4/ISO/SP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrizione: profilo semplice ISO MPEG4 (DivX4)
- Identificatori FourCC o WAV: MP4V

ID Matroska: V_MPEG4/ISO/AP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrizione: profilo semplice avanzato ISO MPEG4 (DivX5, MigrazioniD, FFMPEG)
- Identificatori FourCC o WAV: MP4V


ID Matroska: V_MPEGH/ISO/HEVC 

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC
- Descrizione: HEVC/H.265
- Quattro identificatori CC o WAV: 

ID Matroska: V_VP8

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80
- Descrizione: Formato codec VP8
- Identificatori FourCC o WAV: VP80

ID Matroska: V_VP9

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90
- Descrizione: Formato codec VP9
- Identificatori FourCC o WAV: VP90

ID Matroska: V_MJPEG

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG
- Descrizione: Motion JPEG
- Identificatori FourCC o WAV: MJPG

ID Matroska: V_AV1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1
- Descrizione: AOMedia Video 1
- Identificatori FourCC o WAV: AV01

### <a name="audio-codec-support-for-mkv"></a>Supporto di codec audio per MKV

ID Matroska: A_AAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Descrizione: AAC (Advanced Audio Coding)
- Identificatori FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC

ID Matroska: A_AC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3
- Descrizione: Dolby AC3
- Identificatori FourCC o WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF

ID Matroska: A_MPEG/L3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3
- Descrizione: MPEG Audio Layer-3 (MP3)
- Identificatori FourCC o WAV: WAVE_FORMAT_MPEGLAYER3

ID Matroska: A_MPEG/L1

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Descrizione: payload audio MPEG-1
- Identificatori FourCC o WAV: WAVE_FORMAT_MPEG

ID Matroska: A_PCM/INT/BIG

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descrizione: audio PCM non compresso
- Identificatori FourCC o WAV: WAVE_FORMAT_PCM

ID Matroska: A_PCM/INT/LIT

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descrizione: audio PCM non compresso
- Identificatori FourCC o WAV: WAVE_FORMAT_PCM

ID Matroska: A_PCM/FLOAT/IEEE

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float
- Descrizione: Audio a virgola mobile IEEE non compresso
- Identificatori FourCC o WAV: WAVE_FORMAT_IEEE_FLOAT

ID Matroska: A_ALAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC
- Descrizione: Codec audio senza perdita di Apple
- Identificatori FourCC o WAV: 

ID Matroska: A_MPEG/L2

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Descrizione: MPEG Audio 1, 2 Livello II
- Identificatori FourCC o WAV: WAVE_FORMAT_MPEG

ID Matroska: A_DTS

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD
- Descrizione: Digital Theater System
- Identificatori FourCC o WAV: WAVE_FORMAT_DTS

ID Matroska: A_OPUS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus
- Descrizione: Opus
- Identificatori FourCC o WAV: WAVE_FORMAT_OPUS

ID Matroska: A_VORBIS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis
- Descrizione: Vorbis
- Identificatori FourCC o WAV: 

ID Matroska: A_FLAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC
- Descrizione: Codec audio senza perdita gratuita
- Identificatori FourCC o WAV: WAVE_FORMAT_FLAC

ID Matroska: A_AAC/MAIN

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Descrizione: Codifica audio avanzata (AAC)
- Identificatori FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC

ID Matroska: A_EAC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus
- Descrizione: Ac-3 migliorato
- Identificatori FourCC o WAV: 

ID Matroska: A_TRUEHD

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD
- Descrizione: Dolby TrueHD
- Identificatori FourCC o WAV: 

ID Matroska: A_MS/ACM

- MSFT Media Foundation MF_MT_SUBTYPE: Mappe a diversi WAVE_FORMAT audio definiti in mmreg.h


### <a name="subtitles-codec-support-for-mkv"></a>Supporto dei codec sottotitoli per MKV

ID Matroska: S_TEXT/ASCII

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Descrizione: testo ASCII

ID Matroska: S_TEXT/UTF8

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Descrizione: testo normale UTF-8

ID Matroska: S_TEXT/SSA

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Descrizione: Formato sottotitoli

ID Matroska: S_TEXT/ASS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Descrizione: Formato sottotitoli avanzato

ID Matroska: S_VOBSUB

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub
- Descrizione: Sottotitoli VobSub

ID Matroska: S_HDMV/PGS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS
- Descrizione: sottotitoli grafici di presentazione HDMV (PGS)


## <a name="technical-details-regarding-codecs"></a>Dettagli tecnici relativi ai codec

Per informazioni tecniche sui codec, vedere quanto segue.

- [Specifiche del codec Matroska](http://www.matroska.org/technical/specs/codecid/index.html)
- [GUID del sottotipo audio](audio-subtype-guids.md)
- [GUID del sottotipo video](video-subtype-guids.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> </dl>

 

 



