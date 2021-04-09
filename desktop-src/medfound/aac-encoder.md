---
description: Il codificatore Microsoft Media Foundation AAC è una trasformazione di Media Foundation che codifica il profilo Advanced Audio Coding (AAC) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificatore AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879401"
---
# <a name="aac-encoder"></a>Codificatore AAC

Il codificatore Microsoft Media Foundation AAC è una [trasformazione di Media Foundation](media-foundation-transforms.md) che codifica il profilo Advanced Audio Coding (AAC) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 audio Part 7).

Il codificatore AAC non supporta la codifica in altri profili AAC, ad esempio Main, SSR o LTP.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore AAC è **CLSID \_ AACMFTEncoder**, definito nel file di intestazione wmcodecdsp. h.

## <a name="media-types"></a>Tipi di supporto

Il codificatore AAC supporta i seguenti tipi di supporti. È possibile impostare prima i tipi in base al tipo di input dell'ordine o al tipo di output.

### <a name="input-types"></a>Tipi di input

Impostare gli attributi seguenti sul tipo di supporto di input.



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
<td>Sottotipo.</td>
<td>Deve essere <strong>MFAudioFormat_PCM</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>BITS per campione.</td>
<td>Deve essere 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Campioni al secondo.</td>
<td>Sono supportati i valori seguenti:
<ul>
<li>44100 (44,1 KHz)</li>
<li>48000 (48 KHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali.</td>
<td>Deve essere 1 (mono) o 2 (stereo) o 6 (5,1).
<blockquote>
[!Note]<br />
Il supporto per 6 canali audio è stato introdotto con Windows 10 e non è disponibile per le versioni precedenti di Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Dopo aver impostato il tipo di input, il codificatore deriva i valori seguenti e li aggiunge al tipo di supporto:

-   [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Tipi di output

Impostare gli attributi seguenti sul tipo di supporto di output.



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
<td>Deve essere <strong>MFAudioFormat_AAC</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>BITS per campione.</td>
<td>Deve essere 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Campioni al secondo.</td>
<td>Deve corrispondere al tipo di input.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali.</td>
<td>Deve corrispondere al tipo di input.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocità in bit del flusso AAC codificato, in byte al secondo.</td>
<td>Sono supportati i valori seguenti:
<ul>
<li>12000</li>
<li>16000</li>
<li>20000</li>
<li>24000</li>
</ul>
Il valore predefinito per mono e stereo è 12000 (96 Kbps).<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo di payload AAC.</td>
<td>facoltativo. Se impostato, il valore deve essere zero, a indicare che il flusso contiene solo raw_data_block elementi.<br/> facoltativo. Se l'attributo non è impostato, il valore predefinito è zero, che indica che il flusso contiene solo raw_data_block elementi (AAC non elaborato). <br/> In Windows 7, se l'attributo è impostato, il valore deve essere zero.<br/> A partire da Windows 8, il valore può essere 0 (AAC non elaborato) o 1 (ADTS AAC). <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Il profilo audio AAC e il livello.</td>
<td>facoltativo. Sono supportati i valori seguenti:
<ul>
<li>0x29 (impostazione predefinita)</li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2C</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

Nella tabella seguente sono elencati i valori che è possibile utilizzare per l'attributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.

| Valore MF_MT_AAC_PROFILE_LEVEL_INDICATION | Profilo                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Profilo AAC L2                    | 
| 0x2A                                     | Profilo AAC L4                    | 
| 0x2B                                     | Profilo AAC L5                    | 
| 0x2C                                     | Profilo AAC V1 ad alta efficienza L2 | 
| 0x2E                                     | Profilo AAC V1 ad alta efficienza | 
| 0x2F                                     | Profilo AAC ad alta efficienza V1 L5 | 
| 0x30                                     | Profilo AAC v2 ad alta efficienza L2 | 
| 0x31                                     | Profilo AAC v2 ad efficienza elevata L3 | 
| 0x32                                     | Profilo AAC v2 ad alta efficienza | 
| 0x33                                     | Profilo AAC v2 ad alta efficienza (L5) | 

 

Dopo aver impostato il tipo di output, il codificatore AAC aggiorna il tipo aggiungendo l'attributo [**\_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) . Questo attributo contiene la parte della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) visualizzata dopo la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (ovvero dopo il membro **wfx** ). Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.

Ogni esempio di output contiene un frame AAC compresso senza intestazione. Questo formato è equivalente all'elemento del \_ blocco di dati non elaborati \_ () definito da MPEG-2. L'attributo del [ \_ tipo di payload MF mt \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , se presente nel tipo di output, deve essere impostato su zero per indicare questo tipo di payload.

Ogni esempio di output contiene un frame AAC compresso corrispondente a esempi di PCM 1024. Ad esempio, alla frequenza di campionamento di 48 kHz, la durata di un frame compresso è 21,33 msec.

Se [il \_ \_ tipo di \_ payload \_ MF mt AAC](mf-mt-aac-payload-type.md) è zero (valore predefinito), ogni esempio di output contiene un \_ \_ elemento di blocco di dati non elaborati () come definito da ISO/IEC 13818-7.

## <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio dei tipi di supporti necessari per codificare dall'audio stereo a 44,1 kHz a 160 kbps a AAC non elaborato

Tipo di supporto di input:



| Attributo                                                                                    | Valore                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (facoltativo)      |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)             | 4 (facoltativo)           |
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md)         | 1 (facoltativo)           |
| [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (facoltativo)     |
| [**\_esempi di \_ \_ dimensioni fisse MF mt \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (facoltativo)           |



 

Tipo di supporto di output:



| Attributo                                                                                      | Valore                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                                      | **\_Audio MFMediaType**                                                                          |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [\_tipo di payload MF mt \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                       | 0 (facoltativo)                                                                                    |
| [\_ \_ \_ \_ \_ indicazione livello profilo audio MF mt \_ AAC](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (facoltativo)                                                                                 |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)               | 1 (facoltativo)                                                                                    |
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md)           | 0 (facoltativo)                                                                                    |
| [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (facoltativo)                                                                               |
| [**\_ \_ dati utente MF \_ mt**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} opzionale |



 

## <a name="remarks"></a>Commenti

Nell'implementazione corrente ogni esempio di input deve avere un'ora e una durata valide. Per impostare l'ora di esempio, chiamare [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Per impostare la durata del campione, chiamare [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Se l'ora di esempio non è impostata, il metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificatore restituisce **MF \_ E \_ nessun \_ \_ timestamp di esempio**. Se la durata di esempio non è impostata, il metodo **ProcessInput** restituisce la **\_ durata MF E \_ nessun \_ campione \_**.

La durata campione può essere calcolata come segue:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



dove *nAudioSamplesPerChannel* è il numero di campioni audio PCM per canale nel buffer di input e *nSamplesPerSec* è la frequenza di campionamento, in campioni al secondo.

> [!Note]  
> A causa di un bug nell'implementazione corrente, se la durata dell'esempio è impostata su zero, la chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ha esito positivo, ma una chiamata successiva a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) genererà un'eccezione di divisione per zero. Per evitare questo errore, impostare un periodo di validità diverso da zero per ogni esempio di input.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[**Decoder AAC**](aac-decoder.md)
</dt> <dt>

[Tipi di supporti AAC](aac-media-types.md)
</dt> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

