---
description: GUID del sottotipo audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID del sottotipo audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484132"
---
# <a name="audio-subtype-guids"></a>GUID del sottotipo audio

Sono definiti i seguenti GUID del sottotipo audio. Per specificare il sottotipo, impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) sul tipo di supporto. Eccetto dove indicato, queste costanti sono definite nel file di intestazione mfapi. h.

Quando si usano questi sottotipi, impostare l'attributo [di \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md) su **MFMediaType \_ audio**.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrizione</th>
<th>Tag Format (FOURCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>Codifica audio avanzata (AAC).<br/> Questo sottotipo viene usato per AAC contenuto in un file AVI con un tag di formato audio uguale a 0x00FF. <br/> Per altre informazioni, vedere <a href="aac-decoder.md"><strong>decoder AAC</strong></a>.<br/> Definito in wmcodecdsp. h<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Codifica audio avanzata (AAC).<br/>
<blockquote>
[!Note]<br />
Equivale a MEDIASUBTYPE_MPEG_HEAAC, definito in wmcodecdsp. h.
</blockquote>
<br/> Il flusso può contenere dati AAC non elaborati o dati AAC in un flusso ADTS (Audio Data Transport Stream).<br/> Per altre informazioni, vedere:<br/>
<ul>
<li><a href="aac-decoder.md"><strong>Decoder AAC</strong></a></li>
<li><a href="mpeg-4-file-source.md">Origine file MPEG-4</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>Non usato.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Codec audio Apple Lossless<br/> Supportato in Windows 10 e versioni successive.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Audio multifrequenza adattativi<br/> Supportato in Windows 8.1 e versioni successive.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Audio a banda larga multifrequenza adattativi<br/> Supportato in Windows 8.1 e versioni successive.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>Supportato in Windows 8.1 e versioni successive.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> Stesso valore GUID di <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, definito in ksuuids. h<br/></td>
<td>Nessuna.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Audio Dolby AC-3 sull'interfaccia digitale Sony/Philips (S/PDIF).<br/> Questo valore GUID è identico ai sottotipi seguenti:<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definito in ksmedia. h.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definito in UUIDs. h.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital Plus.<br/> Stesso valore GUID di <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, definito in wmcodecdsp. h.<br/></td>
<td>nessuno</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Dati audio crittografati usati con il percorso audio protetto.</td>
<td>WAVE_FORMAT_DRM (ad esempio 0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Audio di Digital Theater Systems (DTS).</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Codec audio lossless gratuito<br/> Supportato in Windows 10 e versioni successive.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio a virgola mobile IEEE non compresso.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Audio a virgola mobile IEEE non compresso.</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>MPEG Audio Layer-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>Payload audio MPEG-1.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Codec Windows Media Audio 9 Voice.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> Supportato in Windows 10 e versioni successive.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Audio PCM non compresso.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>Audio di QCELP (codice Qualcomm Excited Linear Prediction).</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Codec Windows Media Audio 9 Professional su S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Codec Windows Media Audio 9 Lossless o Windows Media Audio Codec 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Windows Media Audio 8 codec, il codec Windows Media Audio 9 o il codec Windows Media Audio 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Codec Windows Media Audio 9 Professional o Windows Media Audio Codec Professional 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

I tag di formato elencati nella terza colonna di questa tabella vengono utilizzati nella struttura **WAVEFORMATEX** e vengono definiti nel file di intestazione mmreg. h.

Dato un tag di formato audio, è possibile creare un GUID del sottotipo audio come indicato di seguito:

1.  Iniziare con il valore **MFAudioFormat \_ base**, definito in mfaph. i.
2.  Sostituire il primo **valore DWORD** del GUID con il tag di formato.

È possibile usare la [**macro \_ MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) per definire una nuova costante GUID che segue questo modello.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID di tipo multimediale](media-type-guids.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 




