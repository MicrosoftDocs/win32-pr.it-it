---
description: Il codificatore audio Dolby è una trasformazione Media Foundation (MFT) che codifica audio mono o stereo in Dolby Digital, detto anche Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificatore audio digitale Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d14a434481a94021617f04e4cb9e10329ad20a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483097"
---
# <a name="dolby-digital-audio-encoder"></a>Codificatore audio digitale Dolby

Il codificatore audio Dolby è una [trasformazione Media Foundation](media-foundation-transforms.md) (MFT) che codifica audio mono o stereo in Dolby Digital, detto anche Dolby AC-3. Il codificatore non supporta l'input multicanale, ad esempio la configurazione del canale 5.1.

> [!IMPORTANT]
> Per le versioni di Windows precedenti Windows 8, l'implementazione Microsoft della tecnologia Dolby Digital è limitata ai termini del programma di licenza Dolby Digital che le applicazioni Microsoft possono usare.

 

Per altre informazioni sull'audio digitale Dolby, vedere il documento ATSC (Advanced Television Systems Committee) *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore audio Dolby è **\_ CLSID CMSDolbyDigitalEncMFT,** definito nel file di intestazione wmcodecdsp.h.

## <a name="output-types"></a>Tipi di output

Il tipo di output deve essere impostato prima del tipo di input. Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.




| Attributo | Descrizione | Osservazioni | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principale. | Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Sottotipo audio. | Obbligatorio. Deve essere <strong>MFAudioFormat_Dolby_AC3</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Esempi al secondo. | Obbligatorio. Sono supportati i valori seguenti:<ul><li>32000</li><li>44100</li><li>48000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Numero di canali. | Obbligatorio. Deve essere 1 (mono) o 2 (stereo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Specifica l'assegnazione dei canali audio alle posizioni del parlante. | facoltativo. Se impostato, il valore deve essere 0x3 stereo (canali anteriore sinistro e destro) o 0x4 per mono (canale centrale anteriore). | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocità in bit del flusso AC-3 codificato, in byte al secondo. | facoltativo. Per i valori validi, vedere Note. Se questo attributo non è impostato, il codificatore usa una velocità in bit predefinita, come descritto in Osservazioni. | 




 

Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.

## <a name="input-types"></a>Tipi di input

Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.




| Attributo | Descrizione | Osservazioni | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principale. | Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Sottotipo audio. | Obbligatorio. Deve essere <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Numero di bit per campione audio. | Obbligatorio. Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>o 32 se il sottotipo è <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Esempi al secondo. | Obbligatorio. Deve corrispondere al tipo di output. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Numero di canali. | Obbligatorio. Deve corrispondere al tipo di output. | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Allineamento del blocco, in byte. | Obbligatorio. Calcolare il valore nel modo seguente:<ul><li><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</li><li><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</li></ul> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocità in bit del flusso AC3 codificato, in byte al secondo. | Obbligatorio. Deve essere uguale all'allineamento × al secondo. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Specifica l'assegnazione dei canali audio alle posizioni del parlante. | facoltativo. Se impostato, il valore deve corrispondere al tipo di output. | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Numero di bit validi di dati audio in ogni campione audio. | facoltativo. Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>. | 




 

Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono.

## <a name="remarks"></a>Commenti

Ogni frame audio Dolby AC-3 contiene 1536 campioni audio per canale. Tuttavia, ogni buffer di input per il codificatore può contenere un numero qualsiasi di esempi PCM. Le dimensioni di ogni buffer di input devono essere un multiplo dell'allineamento del blocco. Il codificatore memorizza nella cache gli esempi di input fino a quando non è sufficiente per 1536 campioni audio per canale. a quel punto il codificatore restituisce un frame AC-3.

Ogni buffer di output contiene un frame AC-3 non elaborato. La durata equivale alla durata di 1536 campioni PCM alla frequenza di campionamento corrente (32 msec) a una frequenza di campionamento di 48 kHz, 34,83 msec a 44,1 kHz e 48 msec a 32 kHz. Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.

Per specificare la velocità in bit di codifica, impostare l'attributo [ \_ MF MT \_ AUDIO \_ AVG \_ BYTES PER \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di output. La tabella seguente illustra la relazione tra velocità in bit di codifica e MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO.



| Velocità in bit (kbps) | [MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | Commenti                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Solo Mono.                                              |
| 80              | 10000                                                                                    | Solo Mono.                                              |
| 96              | 12000                                                                                    | Solo Mono.                                              |
| 112             | 14000                                                                                    | Solo Mono.                                              |
| 128             | 16000                                                                                    | Mono o stereo.                                         |
| 160             | 20000                                                                                    | Mono o stereo.                                         |
| 192             | 24000                                                                                    | Mono o stereo. Si tratta dell'impostazione predefinita per mono.   |
| 224             | 28000                                                                                    | Mono o stereo.                                         |
| 256             | 32000                                                                                    | Mono o stereo. Si tratta dell'impostazione predefinita per stereo. |
| 320             | 40000                                                                                    | Solo stereo.                                            |
| 384             | 48000                                                                                    | Solo stereo.                                            |
| 448             | 56000                                                                                    | Solo stereo.                                            |



 

La velocità in bit di codifica predefinita è impostata su 256 kbps per stereo e 192 kbps per mono. Le impostazioni predefinite si riflettono nei tipi di supporti restituiti dal metodo [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) del codificatore.

### <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio dei tipi di supporti necessari per codificare l'audio stereo a 48 kHz e pcM intero a 16 bit alla velocità in bit predefinita di 256 kbps.

Tipo di supporto di output:

| Attributo                                                                           | valore                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**        |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo di supporto di input:

| Attributo                                                                                | valore                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 




