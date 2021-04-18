---
description: Il decoder audio Dolby è un Media Foundation Transform (MFT) che codifica mono o stereo audio in Dolby Digital, detto anche Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificatore audio Dolby Digital
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305398"
---
# <a name="dolby-digital-audio-encoder"></a>Codificatore audio Dolby Digital

Il decoder audio Dolby è un [Media Foundation Transform](media-foundation-transforms.md) (MFT) che codifica mono o stereo audio in Dolby Digital, detto anche Dolby AC-3. Il codificatore non supporta l'input multicanale, ad esempio la configurazione del canale 5,1.

> [!IMPORTANT]
> Per le versioni di Windows precedenti a Windows 8, l'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

 

Per ulteriori informazioni sull'audio Dolby Digital, vedere la sezione relativa alla revisione B per il documento ATSC (Advanced Television Systems Committee), *ovvero AC-3, E-AC-3*.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del decodificatore Dolby audio è **CLSID \_ CMSDolbyDigitalEncMFT**, definito nel file di intestazione wmcodecdsp. h.

## <a name="output-types"></a>Tipi di output

Il tipo di output deve essere impostato per primo, prima del tipo di input. Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Deve essere <strong>MFAudioFormat_Dolby_AC3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Campioni al secondo.</td>
<td>Obbligatorio. Sono supportati i valori seguenti:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali.</td>
<td>Obbligatorio. Deve essere 1 (mono) o 2 (stereo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se impostato, il valore deve essere 0x3 per i canali stereo (front left e Right) o 0x4 per mono (canale front-end).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso AC-3 codificato, in byte al secondo.</td>
<td>facoltativo. Vedere la sezione Osservazioni per i valori validi. Se questo attributo non è impostato, il codificatore usa una velocità in bit predefinita, come descritto in note.</td>
</tr>
</tbody>
</table>



 

Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.

## <a name="input-types"></a>Tipi di input

Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Deve essere <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Numero di bit per esempio audio.</td>
<td>Obbligatorio. Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>, oppure 32 se il sottotipo è <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Campioni al secondo.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Allineamento del blocco in byte.</td>
<td>Obbligatorio. Calcolare il valore come segue:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso AC3 codificato, in byte al secondo.</td>
<td>Obbligatorio. È necessario che l'allineamento a blocchi sia uguale a × campioni al secondo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se impostato, il valore deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Numero di bit validi di dati audio in ogni esempio audio.</td>
<td>facoltativo. Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono.

## <a name="remarks"></a>Commenti

Ogni frame audio Dolby AC-3 contiene 1536 di esempi audio per canale. Ogni buffer di input per il codificatore può tuttavia contenere un numero qualsiasi di campioni PCM. La dimensione di ogni buffer di input deve essere un multiplo dell'allineamento del blocco. Il codificatore memorizza nella cache gli esempi di input fino a quando non dispone di un numero sufficiente di campioni audio 1536 per canale; a questo punto il codificatore restituisce un frame AC-3.

Ogni buffer di output contiene un frame AC-3 non elaborato. La durata è equivalente alla durata di 1536 campioni PCM alla frequenza di campionamento corrente (32 msec) alla frequenza di campionamento 48 kHz, 34,83 msec a 44,1 kHz e 48 msec a 32 kHz. Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.

Per specificare la velocità in bit di codifica, impostare l'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di output. La tabella seguente illustra la relazione tra la velocità in bit di codifica e i \_ \_ byte media audio MF mt \_ \_ \_ al \_ secondo.



| Velocità in bit (Kbps) | [\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) | Commenti                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Solo mono.                                              |
| 80              | 10000                                                                                    | Solo mono.                                              |
| 96              | 12000                                                                                    | Solo mono.                                              |
| 112             | 14000                                                                                    | Solo mono.                                              |
| 128             | 16000                                                                                    | Mono o stereo.                                         |
| 160             | 20000                                                                                    | Mono o stereo.                                         |
| 192             | 24000                                                                                    | Mono o stereo. Questa è l'impostazione predefinita per mono.   |
| 224             | 28000                                                                                    | Mono o stereo.                                         |
| 256             | 32000                                                                                    | Mono o stereo. Questa è l'impostazione predefinita per stereo. |
| 320             | 40000                                                                                    | Solo stereo.                                            |
| 384             | 48000                                                                                    | Solo stereo.                                            |
| 448             | 56000                                                                                    | Solo stereo.                                            |



 

La velocità in bit di codifica predefinita è impostata su 256 kbps per stereo e 192 kbps per mono. Le impostazioni predefinite sono riflesse nei tipi di supporto restituiti dal metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) del codificatore.

### <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio dei tipi di supporto necessari per codificare un PCM a 16 bit di tipo Integer, audio stereo 48-kHz alla velocità in bit predefinita di 256 kbps.

Tipo di supporto di output:

| Attributo                                                                           | Valore                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**        |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo di supporto di input:

| Attributo                                                                                | Valore                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [\_ \_ bit audio MF \_ mt \_ per \_ campione](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_ \_ \_ allineamento blocchi audio MF \_ mt](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 




