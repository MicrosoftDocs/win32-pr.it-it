---
description: 'Questo filtro decodifica i formati audio seguenti:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Decodificatore audio MICROSOFT MPEG-1/DD/AAC (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd20bfc2ad8a366b46ac0c0600d8cc7a8bca5abacae621e8ea7d02f5f1cb4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051251"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Decodificatore audio MPEG-1/DD/AAC Microsoft

Questo filtro decodifica i formati audio seguenti:

-   Livelli audio MPEG-1 I e II.
-   Audio MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), solo mono e stereo.
-   Profilo AAC (Advanced Audio Coding) Low Complexity (LC).
-   High-Efficiency AAC (HE-AAC) versione 1 e 2.
-   DTS (Digital Theater Systems) pass-through per l'output digitale.
-   Solo LPCM, mono e stereo, con o senza intestazioni PES.
-   Dolby Digital.
-   Dolby Digital Plus, inclusa la conversione da Dolby Digital Plus a Dolby Digital per l'output digitale.

> [!Note]  
> L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai termini del programma di licenza Dolby Digital che le applicazioni Microsoft possono usare.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 

La decodifica dei formati Dolby Digital Plus, AAC e HE-AAC richiede Windows 7. La decodifica di Dolby Digital o Dolby Digital Plus non è supportata in Windows 7 Home Basic o Windows 7 Starter.

Nel Registro di sistema il nome descrittivo di questo filtro è "Decodificatore audio DTV-DVD Microsoft".



Filtrare le informazioni

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipi di supporti pin di input

In Windows Vista e versioni successive, il filtro supporta i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1Payload**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK,** **MEDIASUBTYPE \_ DOLBY \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK,** **MEDIASUBTYPE \_ DTS** (vedere la nota 2).
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK,** **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES,** **MEDIASUBTYPE \_ DOLBY \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ MPEG2 \_ PES,** **MEDIASUBTYPE \_ DTS** (vedere la nota 2).
-   **MEDIATYPE \_ MPEG2 \_ PES,** **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**

A partire Windows 7, il filtro supporta anche i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (vedere la nota 1).
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DTS2** (vedere la nota 2).
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DVM** (vedere la nota 1).
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ AUDIO,** **MEDIASUBTYPE \_ MPEG \_ LOAS**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (vedere la nota 1).
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG \_ LOAS**

Il tipo di input può cambiare dinamicamente durante lo streaming.<br/> Per altre informazioni su questi tipi di supporti, vedere [**Sottotipi audio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai termini del programma di licenza Dolby Digital che le applicazioni Microsoft possono usare.

<br/>

> [!Note]  
> 2. Per l'input DTS (Digital Theater Systems), è supportato solo l'output S/PDIF (DTS su S/PDIF). La decodifica audio non è supportata.

<br/>

Interfacce pin di input

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

In Windows Vista e versioni successive, il filtro supporta i tipi di output seguenti:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3 \_ SPDIF** (uguale a **KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DOLBY \_ DIGITAL**)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ PCM**

A partire Windows 7, il filtro supporta anche i tipi di output seguenti:<br/>

-   **MEDIATYPE \_ Audio,** **KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ IEEE \_ FLOAT**

Interfacce pin di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtro CLSID

**CLSID \_ CMPEG2AudDecoderDS** (dichiarato in wmcodecdsp.h)

File eseguibile

msmpeg2adec.dll

[Merito](merit.md)

**MERITO \_ NORMAL** - 1

[Categoria filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> Una versione precedente della documentazione ha dichiarato che questo filtro può decodificare "audio MPEG-2". Il filtro decodifica solo l'audio MPEG-2 compatibile con le versioni precedenti.

 

## <a name="remarks"></a>Commenti

I flussi Mono vengono sempre decodificati in stereo.

Per i flussi con una configurazione del canale di due o più altoparlanti, il decodificatore esegue una delle operazioni seguenti:

-   Combina fino a sei canali, usando la configurazione comune degli altoparlanti 5.1.
-   Downmix in stereo.

Per selezionare tra queste due opzioni, usare [**l'interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per impostare la proprietà [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) prima di connettere i pin. In alternativa, quando l'applicazione compila il grafico dei filtri, può impostare il tipo di supporto desiderato sul segnaposto di output.

### <a name="aac-decoding"></a>Decodifica AAC

Per AAC, il decodificatore ha determinati vincoli di formato sull'input AAC compresso. Questi vincoli di formato sono gli stessi Media Foundation [**decodificatore AAC**](../medfound/aac-decoder.md)e sono documentati nella sezione "[**Vincoli di formato**](../medfound/aac-decoder.md)".

Il DirectShow decodificatore accetta anche tipi di input diversi rispetto Media Foundation decodificatore. Il DirectShow decodificatore supporta i tipi di input AAC seguenti:

-   **MEDIASUBTYPE \_ RAW \_ AAC1:** AAC non elaborato, in genere disponibile in AVI o Matroska (. MKV).
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC:** AAC in un flusso di trasporto dati audio (ADTS) per lo streaming.
-   **MEDIASUBTYPE \_ \_LOAS MPEG:** flusso di trasporto con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).

Il Media Foundation decodificatore supporta i tipi di input AAC seguenti:

-   MFAudioFormat \_ AAC (uguale a **MEDIASUBTYPE \_ MPEG \_ HEAAC)** per la riproduzione di file MP4.
-   **MEDIASUBTYPE \_ RAW \_ AAC1**.

### <a name="property-sets"></a>Set di proprietà

Il pin di input del decodificatore supporta i seguenti set di proprietà tramite [**IKsPropertySet:**](ikspropertyset.md)

-   [**Set di proprietà protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Rate-Change Property Set**](rate-change-property-set.md).

> [!Note]  
> A partire da Windows 7, il decodificatore supporta la modalità trick tramite il set di proprietà rate-change. Supporta le frequenze di riproduzione nell'intervallo \[ da 0,501 a 2,0, dove 1,0 è la frequenza di riproduzione normale e 2,0 è il doppio della frequenza \] normale.

 

### <a name="codec-properties"></a>Proprietà codec

Il pin di input del decodificatore supporta le proprietà seguenti tramite [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Proprietà                                                          | Richiede                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Windows Solo Vista; non supportato in Windows 7 o versioni successive. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Il filtro supporta le proprietà seguenti tramite [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Proprietà                                                                          | Richiede      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (vedere la nota 3). | Windows Vista |
| [**AVDecdDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecdDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. La [**proprietà AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) deve essere impostata prima che il pin di output del decodificatore sia connesso. In caso contrario, la modifica non ha alcun effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows solo 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sottotipi audio**](audio-subtypes.md)
</dt> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti DVD**](dvd-media-types.md)
</dt> </dl>

 

 
