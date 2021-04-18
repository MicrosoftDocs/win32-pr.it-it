---
description: 'Il decodificatore Microsoft Media Foundation AAC è una trasformazione Media Foundation che decodifica i profili AAC (Advanced Audio Coding) ed High Efficiency AAC (HE-AAC) seguenti:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decoder AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306768"
---
# <a name="aac-decoder"></a>Decoder AAC

Il decodificatore Microsoft Media Foundation AAC è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica i profili AAC (Advanced Audio Coding) ed High Efficiency AAC (HE-AAC) seguenti:

-   Profilo MPEG-2 AAC con complessità bassa (LC) (multicanale).
-   MPEG-4 HE-AAC V1 (multicanale) con AAC-LC core.
-   MPEG-4 HE-AAC v2 (stereo) con AAC-LC core.

Il decodificatore AAC supporta entrambi i flussi AAC non elaborati senza intestazioni e AAC in un flusso di trasporto dati audio (ADTS).

A partire da Windows 8, il decodificatore AAC supporta anche la decodifica dei flussi di trasporto audio MPEG-4 con un livello multiplex (LATM) e un livello di sincronizzazione (LOAS). Può anche convertire un flusso LATM/LOAS in ADTS.

## <a name="media-types"></a>Tipi di supporto

Il decodificatore AAC supporta i seguenti tipi di supporti.

### <a name="input-types"></a>Tipi di input

Il decodificatore AAC supporta i sottotipi audio seguenti:



| Subtype                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Intestazione       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC non elaborato o ADTS AAC.<br/> Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione degli strumenti di replica della banda spettrale (SBR) e dello stereo parametrico (PS), se presenti. L'effetto dello strumento SBR consiste nel raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC di base. L'effetto dello strumento PS è la decodifica dello stereo da un flusso AAC-LC Core mono-Channel.<br/> Questo sottotipo è equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definito in wmcodecdsp. h. Vedere [GUID del sottotipo audio](audio-subtype-guids.md). <br/> L' [origine file MPEG-4](mpeg-4-file-source.md) e il parser ADTS restituiscono questo sottotipo. <br/> | mfapi. h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC non elaborato. <br/> Questo sottotipo viene usato per AAC contenuto in un file AVI con tag di formato audio uguale a WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp. h |



 

Per configurare il decodificatore AAC, impostare i seguenti attributi sul tipo di supporto di input.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
<th>Osservazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principale.</td>
<td>Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Sottotipo audio.</td>
<td>Per informazioni dettagliate, vedere la descrizione precedente.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Profilo audio e livello. <br/></td>
<td>facoltativo. Si applica solo ai <strong>MFAudioFormat_AAC</strong>. <br/> Il valore di questo attributo è il campo <strong>audioProfileLevelIndication</strong> , come definito da ISO/IEC 14496-3. <br/> Se è sconosciuto, impostare su zero o 0xFE ( &quot; nessun profilo audio specificato &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo di payload.<br/></td>
<td>Si applica solo ai <strong>MFAudioFormat_AAC</strong>. Il decodificatore supporta i tipi di payload seguenti: <br/>
<ul>
<li>0: AAC non elaborato. Il flusso contiene solo gli elementi raw_data_block (), come definito da MPEG-2.</li>
<li>1: ADTS. Il flusso contiene un adts_sequence (), come definito da MPEG-2. È consentita una sola raw_data_block () per adts_frame ().</li>
<li>3: flusso del trasporto audio con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM). Dei tre tipi di LOAS, è supportato solo <strong>AudioSyncStream</strong> . Il livello multiplex è <strong>AudioMuxElement</strong>, limitato a un solo programma audio e a un livello.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> è facoltativo. Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo elementi raw_data_block.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profondità di bit desiderata dell'audio PCM decodificato.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Per altre informazioni, vedere <a href="#format-constraints">vincoli di formato</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali, incluso il canale LFE (Low Frequency), se presente.<br/></td>
<td>L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Frequenza di campionamento, in campioni al secondo.<br/></td>
<td>L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Ulteriori informazioni sul formato.</td>
<td>Il valore di questo attributo dipende dal sottotipo.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX</strong> (ovvero dopo il membro <strong>wfx</strong> ). Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig (). Devono essere visualizzati i dati. in caso contrario, il decodificatore rifiuterà il tipo di supporto.</li>
</ul>
La lunghezza dei dati di AudioSpecificConfig () è di 2 byte per AAC-LC o HE-AAC con segnalazione implicita di SBR/PS. È più di 2 byte per HE-AAC con segnalazione esplicita di SBR/PS.<br/> Il valore di <strong>audioObjectType</strong> come definito in AudioSpecificConfig () deve essere 2, che indica AAC-LC. Il valore di <strong>extensionAudioObjectType</strong> deve essere 5 per SBR o 29 per PS. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Tipi di output

Il decodificatore supporta i tipi di output seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio a virgola mobile IEEE.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>audio PCM a 16 bit.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Richiede Windows 8. <br/> Questo tipo di output può essere usato per convertire un flusso AAC nel formato LOAS/LATM in formato ADTS. <br/> Per convertire un flusso LOAS/LATM in un flusso ADTS, impostare il tipo di input su <strong>MFAudioFormat_AAC</strong> con payload di tipo 3 (LOAS). Impostare quindi il tipo di output su <strong>MFAudioFormat_AAC</strong> con payload di tipo 1 (ADTS). Il decodificatore riformatterà il Conainter senza decodificare il Bitstream. <br/>
<blockquote>
[!Note]<br />
Il decodificatore non registra <strong>MFAudioFormat_AAC</strong> come tipo di output. Tuttavia, se l'applicazione imposta il tipo di input come descritto, il metodo <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> restituisce <strong>MFAudioFormat_AAC</strong> nell'elenco dei tipi di output disponibili.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Se il flusso di input contiene più di due canali, il decodificatore AAC fornisce due opzioni per il formato di output:

-   La stessa configurazione del canale del tipo di input.
-   Riduzioni stereo.

## <a name="format-constraints"></a>Vincoli di formato

La frequenza di campionamento audio decodificata deve essere una delle seguenti, dopo l'applicazione di SBR (se presente):

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

Le frequenze di campionamento superiori a 48 kHz non sono supportate.

Il decodificatore supporta fino a 6 canali audio. Per ogni configurazione dell'altoparlante, il decodificatore prevede che gli elementi sintattici AAC siano visualizzati in un determinato ordine. Nella tabella seguente sono elencate le configurazioni supportate per i relatori. Nella terza colonna della tabella sono elencati gli elementi sintattici previsti e il relativo ordine, utilizzando la notazione seguente:

-   <SCE1>: Il single_channel_element (SCE) associato all'altoparlante del centro anteriore.
-   <SCE2>: SCE associata all'altoparlante back-Center.
-   <CPE1>: La channel_pair_element (CPE) associata agli altoparlanti anteriori.
-   <CPE2>: CPE associato agli altoparlanti back (o Side)
-   <LFE>: Il lfe_channel_element (LFE).

Per ulteriori informazioni su questi elementi sintattici, vedere ISO/IEC 13818-7.



| Configurazione       | Maschera di canale                                                                                                                                                              | Elementi sintattici AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Stereo o dual mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Per i dati AAC non elaborati, ogni esempio di input deve contenere esattamente un frame compresso AAC completo.

Per ADTS, ogni esempio di input può contenere più frame audio, oltre a frame parziali, i frame possono estendersi sui limiti di esempio. Ogni intestazione ADTS deve essere seguita da un frame AAC.

Il decodificatore AAC non supporta nessuno dei seguenti elementi:

-   Profilo principale, profilo Sample-Rate scalabile (SRS) o profilo di stima a lungo termine (LTP).
-   Formato di interscambio dati audio (ADIF).
-   Flussi di trasporto LATM/LAOS.
-   Elementi del canale di accoppiamento (CCEs). Il decodificatore ignorerà i frame audio con CCEs.
-   AAC-LC con una dimensione del fotogramma 960-Sample. Sono supportati solo i frame 1024-Sample.

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decodificatore AAC implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.



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
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Specifica se l'audio a 2 canali è codificato come stereo o doppia mono. Considera come di sola lettura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Specifica il modo in cui il decodificatore riproduce audio mono doppio. Il valore predefinito è <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: output CH1 sugli altoparlanti sinistro e destro. <br/> Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>Il decodificatore AAC non gestisce le modifiche del formato dinamico e deve essere svuotato o svuotato prima che venga impostato un nuovo tipo di supporto di input. Considerare questo attributo come di sola lettura. <br/>
<blockquote>
[!Note]<br />
Il decodificatore AAC segnala erroneamente un valore <strong>true</strong> per questo attributo.
</blockquote>
<br/> <br/> In Windows 7, il decodificatore segnala erroneamente il valore <strong>true</strong> per l'attributo. In Windows 8, il decodificatore segnala <strong>false</strong>, ovvero il valore corretto<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio del tipo di supporto di input necessario per un flusso AAC-LC a 6 canali, 48-kHz, usando un payload AAC non elaborato:



| Attributo                                                                                      | Valore                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0XB0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2A (facoltativo)                                                                      |



 

I primi 12 byte di [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corrispondono ai seguenti membri della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :

-   **wPayloadType** = 0 (AAC non elaborato)
-   **wAudioProfileLevelIndication** = 0X2a (profilo AAC, livello 4)
-   **wStructType** = 0

Gli ultimi due byte di [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contengono il valore di AudioSpecificConfig (), come definito da MPEG-4.

-   AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bit)
-   AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bit)
-   AudioSpecificConfig. channelConfiguration = 6 (4 bit)
-   GASpecificConfig. frameLengthFlag = 0 (1 bit)
-   GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)
-   GASpecificConfig. extensionFlag = 0 (1 bit)

Dato questo tipo di input, usare il seguente tipo di supporto di output per ottenere audio PCM a virgola mobile a 6 canali a 32 bit dal decodificatore:



| Attributo                                                                                    | Valore                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (facoltativo)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (facoltativo)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3F (facoltativo)          |



 

Se è installato il supplemento di aggiornamento della piattaforma per Windows Vista, il decodificatore audio AAC è disponibile in Windows Vista, ma è accessibile solo in Windows Vista tramite il [lettore di origine](source-reader.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                                                  |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll su Windows 7; </dt> <dt>MSAudDecMFT.dll in Windows 8</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Tipi di supporti AAC](aac-media-types.md)
</dt> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[**Decoder audio Microsoft MPEG-1/gg/AAC**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
