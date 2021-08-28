---
description: Questo argomento descrive come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipi di supporti AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479887"
---
# <a name="aac-media-types"></a>Tipi di supporti AAC

Questo argomento descrive come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.

Per l'audio AAC sono definiti due sottotipi:



| Subtype                     | Descrizione          | Intestazione       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | AAC non elaborato o AAC ADTS. | mfapi.h      |
| **MEDIASUBTYPE \_ RAW \_ AAC1** | AAC non elaborato.             | wmcodecdsp.h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione degli strumenti SBR (Spectral Band Replication) e Parametric Stereo (PS), se presenti. L'effetto dello strumento SBR è raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC principale. L'effetto dello strumento PS è decodificare stereo da un flusso AAC-LC core monocanale.

Questo sottotipo equivale a **MEDIASUBTYPE \_ MPEG \_ HEAAC,** definito in wmcodecdsp.h. Vedere [GUID sottotipo audio](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ RAW \_ AAC1
</dt> <dd>

Questo sottotipo viene usato per AAC contenuto in un file AVI con il tag di formato audio uguale a WAVE \_ FORMAT \_ RAW \_ AAC1 (0x00FF).

Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.

</dd> </dl>

Gli attributi del tipo di supporto seguenti si applicano all'audio AAC.




| Attributo | Descrizione | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principale. Deve essere <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sottotipo audio. Per informazioni dettagliate, vedere la descrizione precedente. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Profilo e livello audio. <br /> Il valore di questo attributo è il campo <strong>audioProfileLevelIndication,</strong> come definito da ISO/IEC 14496-3.<br /> Se sconosciuto, impostare su zero o 0xFE ("nessun profilo audio specificato").<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Velocità in bit del flusso AAC codificato, in byte al secondo. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo di payload.<br /> Si applica solo <strong>a MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> facoltativo. Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo raw_data_block elementi.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profondità in bit dell'audio PCM decodificato. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Assegnazione dei canali audio alle posizioni del parlante. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Numero di canali, incluso il canale a bassa frequenza (LFE), se presente.<br /> L'interpretazione di questo valore dipende dal sottotipo multimediale, come descritto in precedenza.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Frequenza di campionamento, in campioni al secondo.<br /> L'interpretazione di questo valore dipende dal sottotipo multimediale, come descritto in precedenza.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | Il valore di questo attributo dipende dal sottotipo:<br /><ul><li><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX,</strong> ovvero dopo il <strong>membro wfx.</strong> Questi dati sono seguiti dai dati AudioSpecificConfig(), come definito da ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig().</li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Supporto mpeg-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

