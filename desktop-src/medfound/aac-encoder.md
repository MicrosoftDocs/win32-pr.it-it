---
description: Il codificatore AAC Microsoft Media Foundation è una trasformazione Media Foundation che codifica il profilo AAC (Advanced Audio Coding) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 Audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificatore AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb6867ad42645ffc2bbf2b853e215d3794053157a776e02eddf015b320e3215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943371"
---
# <a name="aac-encoder"></a>Codificatore AAC

Il codificatore AAC Microsoft Media Foundation è una trasformazione [Media Foundation](media-foundation-transforms.md) che codifica il profilo AAC (Advanced Audio Coding) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 Audio Part 7).

Il codificatore AAC non supporta la codifica in altri profili AAC, ad esempio Main, SSR o LTP.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore AAC è **CLSID \_ AACMFTEncoder,** definito nel file di intestazione wmcodecdsp.h.

## <a name="media-types"></a>Tipi di supporti

Il codificatore AAC supporta i tipi di supporti seguenti. È possibile impostare prima i tipi nell'ordine del tipo di input o nel tipo di output.

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
<td>Bit per campione.</td>
<td>Deve essere 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Esempi al secondo.</td>
<td>Sono supportati i valori seguenti:
<ul>
<li>44100 (44,1 KHz)</li>
<li>48000 (48 KHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali.</td>
<td>Deve essere 1 (mono) o 2 (stereo) o 6 (5.1).
<blockquote>
[!Note]<br />
Il supporto per 6 canali audio è stato introdotto con Windows 10 e non è disponibile per le versioni precedenti di Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Dopo aver impostato il tipo di input, il codificatore deriva i valori seguenti e li aggiunge al tipo di supporto:

-   [**BYTE MEDIA \_ AUDIO MF MT \_ AL \_ \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**ALLINEAMENTO DEI \_ BLOCCHI AUDIO MF MT \_ \_ \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**VELOCITÀ IN BIT MEDIA MF \_ MT \_ \_**](mf-mt-avg-bitrate-attribute.md)

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
<td>Bit per campione.</td>
<td>Deve essere 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Esempi al secondo.</td>
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
<td>facoltativo. Se impostato, il valore deve essere zero, a indicare che il flusso contiene solo raw_data_block elementi.<br/> facoltativo. Se l'attributo non è impostato, il valore predefinito è zero, a indicare che il flusso contiene solo elementi raw_data_block (controllo di accesso non elaborato). <br/> In Windows 7, se questo attributo è impostato, il valore deve essere zero.<br/> A partire Windows 8, il valore può essere 0 (AAC non elaborato) o 1 (ADTS AAC). <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Livello e profilo audio AAC.</td>
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

Nella tabella seguente sono elencati i valori che possono essere utilizzati per l'MF_MT_AAC_PROFILE_LEVEL_INDICATION attributo .

| MF_MT_AAC_PROFILE_LEVEL_INDICATION valore | Profilo                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Profilo AAC L2                    | 
| 0x2A                                     | Profilo AAC L4                    | 
| 0x2B                                     | Profilo AAC L5                    | 
| 0x2C                                     | High Efficiency v1 AAC Profile L2 | 
| 0x2E                                     | High Efficiency v1 AAC Profile L4 | 
| 0x2F                                     | High Efficiency v1 AAC Profile L5 | 
| 0x30                                     | High Efficiency v2 AAC Profile L2 | 
| 0x31                                     | High Efficiency v2 AAC Profile L3 | 
| 0x32                                     | High Efficiency v2 AAC Profile L4 | 
| 0x33                                     | High Efficiency v2 AAC Profile L5 | 

 

Dopo aver impostato il tipo di output, il codificatore AAC aggiorna il tipo aggiungendo [**l'attributo \_ MF MT \_ USER \_ DATA.**](mf-mt-user-data-attribute.md) Questo attributo contiene la parte della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) visualizzata dopo la [**struttura WAVEFORMATEX,**](/previous-versions/dd757713(v=vs.85)) ovvero dopo il **membro wfx.** Questi dati sono seguiti dai dati AudioSpecificConfig(), come definito da ISO/IEC 14496-3.

Ogni esempio di output contiene un frame AAC compresso senza intestazione. Questo formato equivale all'elemento raw \_ data \_ block() definito da MPEG-2. [L'attributo \_ MF MT \_ AAC PAYLOAD \_ \_ TYPE,](mf-mt-aac-payload-type.md) se presente nel tipo di output, deve essere impostato su zero per indicare questo tipo di payload.

Ogni esempio di output contiene un frame AAC compresso corrispondente a 1024 esempi PCM. Ad esempio, a una frequenza di campionamento di 48 KHz, la durata di un frame compresso è di 21,33 msec.

Se [MF \_ MT \_ AAC PAYLOAD \_ \_ TYPE](mf-mt-aac-payload-type.md) è zero (valore predefinito), ogni esempio di output contiene un elemento raw data block() come definito da \_ \_ ISO/IEC 13818-7.

## <a name="example-media-types"></a>Tipi di supporti di esempio

Ecco un esempio dei tipi di supporti necessari per codificare da 44,1 kHz, audio stereo da 160 Kbps ad AAC non elaborato

Tipo di supporto di input:



| Attributo                                                                                    | Valore                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (facoltativo)      |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 4 (facoltativo)           |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)         | 1 (facoltativo)           |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (facoltativo)     |
| [**ESEMPI DI \_ DIMENSIONI \_ \_ FISSE MF MT \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (facoltativo)           |



 

Tipo di supporto di output:



| Attributo                                                                                      | Valore                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType \_ Audio**                                                                          |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [TIPO DI \_ PAYLOAD MF MT \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                       | 0 (facoltativo)                                                                                    |
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (facoltativo)                                                                                 |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)               | 1 (facoltativo)                                                                                    |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)           | 0 (facoltativo)                                                                                    |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (facoltativo)                                                                               |
| [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (facoltativo) |



 

## <a name="remarks"></a>Commenti

Nell'implementazione corrente ogni esempio di input deve avere un tempo e una durata validi. Per impostare l'ora di esempio, chiamare [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Per impostare la durata del campione, chiamare [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Se l'ora di esempio non è impostata, il metodo [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificatore restituisce **MF \_ E NO SAMPLE \_ \_ \_ TIMESTAMP**. Se la durata del campione non è impostata, il **metodo ProcessInput** restituisce **MF \_ E NO \_ SAMPLE \_ \_ DURATION**.

La durata del campione può essere calcolata nel modo seguente:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



dove *nAudioSamplesPerChannel* è il numero di campioni audio PCM per canale nel buffer di input e *nSamplesPerSec è* la frequenza di campionamento, in campioni al secondo.

> [!Note]  
> A causa di un bug nell'implementazione corrente, se la durata del campione è impostata su zero, la chiamata [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ha esito positivo, ma una chiamata successiva a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) genererà un'eccezione di divisione per zero. Per evitare questo errore, impostare una durata valida diversa da zero in ogni esempio di input.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[**Decodificatore AAC**](aac-decoder.md)
</dt> <dt>

[Tipi di supporti AAC](aac-media-types.md)
</dt> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Supporto mpeg-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

