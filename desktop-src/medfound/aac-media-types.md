---
description: In questo argomento viene descritto come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipi di supporti AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968849"
---
# <a name="aac-media-types"></a>Tipi di supporti AAC

In questo argomento viene descritto come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.

Per audio AAC sono definiti due sottotipi:



| Subtype                     | Descrizione          | Intestazione       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | AAC non elaborato o ADTS AAC. | mfapi. h      |
| **MEDIASUBTYPE \_ RAW \_ AAC1** | AAC non elaborato.             | wmcodecdsp. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione degli strumenti di replica della banda spettrale (SBR) e dello stereo parametrico (PS), se presenti. L'effetto dello strumento SBR consiste nel raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC di base. L'effetto dello strumento PS è la decodifica dello stereo da un flusso AAC-LC Core mono-Channel.

Questo sottotipo è equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, definito in wmcodecdsp. h. Vedere [GUID del sottotipo audio](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ RAW \_ AAC1
</dt> <dd>

Questo sottotipo viene usato per AAC contenuto in un file AVI con il tag di formato audio uguale a WAVE \_ Format \_ RAW \_ AAC1 (0x00FF).

Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.

</dd> </dl>

Gli attributi del tipo di supporto seguenti si applicano all'audio AAC.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principale. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Sottotipo audio. Per informazioni dettagliate, vedere la descrizione precedente.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Profilo audio e livello. <br/> Il valore di questo attributo è il campo <strong>audioProfileLevelIndication</strong> , come definito da ISO/IEC 14496-3.<br/> Se è sconosciuto, impostare su zero o 0xFE ( &quot; nessun profilo audio specificato &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocità in bit del flusso AAC codificato, in byte al secondo.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo di payload.<br/> Si applica solo ai <strong>MFAudioFormat_AAC</strong>.<br/> <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> è facoltativo. Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo elementi raw_data_block.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profondità di bit dell'audio PCM decodificato.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Assegnazione dei canali audio alle posizioni degli oratori.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali, incluso il canale LFE (Low Frequency), se presente.<br/> L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Frequenza di campionamento, in campioni al secondo.<br/> L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Il valore di questo attributo dipende dal sottotipo:<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX</strong> (ovvero dopo il membro <strong>wfx</strong> ). Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig ().</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

