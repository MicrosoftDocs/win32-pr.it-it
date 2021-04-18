---
description: 'Questo filtro decodifica i formati audio seguenti:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Decoder audio Microsoft MPEG-1/gg/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303992"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Decoder audio Microsoft MPEG-1/gg/AAC

Questo filtro decodifica i formati audio seguenti:

-   MPEG-1 Audio Layer I e II.
-   Audio MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), mono e stereo.
-   Profilo di alta complessità (LC, Advanced Audio Coding).
-   High-Efficiency AAC (HE-AAC) versione 1 e versione 2.
-   Digital Theater Systems (DTS) pass-through per l'output digitale.
-   Solo LPCM, mono e stereo, con o senza intestazioni PE.
-   Dolby Digital.
-   Dolby Digital Plus, inclusa la conversione da Dolby Digital Plus a Dolby Digital for Digital output.

> [!Note]  
> L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 

La decodifica dei formati Dolby Digital Plus, AAC e HE-AAC richiede Windows 7. La decodifica di Dolby Digital o Dolby Digital Plus non è supportata in Windows 7 Home Basic o Windows 7 Starter.

Nel registro di sistema il nome descrittivo di questo filtro è "Microsoft DTV-DVD audio decoder".



Informazioni sul filtro

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipi di supporti pin di input

In Windows Vista e versioni successive, il filtro supporta i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**
-   **MEDIATYPE \_ Audio**, **\_ \_ audio MPEG2 MEDIASUBTYPE**
-   **MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ DTS** (vedere la nota 2).
-   **MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ DTS** (vedere la nota 2).
-   **MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MEDIATYPE \_ MPEG2 \_ PE**, **\_ \_ audio MPEG2 MEDIASUBTYPE**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).
-   **MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ \_ audio MPEG2**

A partire da Windows 7, il filtro supporta anche i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vedere la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DTS2** (vedere la nota 2).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVM** (vedere la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ LOAS**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vedere la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ LOAS**

Il tipo di input può variare in modo dinamico durante il flusso.<br/> Per ulteriori informazioni su questi tipi di supporti, vedere [**sottotipi audio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

<br/>

> [!Note]  
> 2. Per l'input DTS (Digital Theater Systems), è supportato solo l'output S/PDIF (DTS su S/PDIF). La decodifica audio non è supportata.

<br/>

Interfacce pin di input

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

In Windows Vista e versioni successive, il filtro supporta i tipi di output seguenti:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (uguale al **\_ sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital**)
-   **MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**

A partire da Windows 7, il filtro supporta anche i tipi di output seguenti:<br/>

-   **MEDIATYPE \_ Audio**, **\_ sottotipo KSDATAFORMAT \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**

Interfacce del PIN di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID filtro

**CLSID \_ CMPEG2AudDecoderDS** (dichiarata in wmcodecdsp. h)

File eseguibile

msmpeg2adec.dll

[Merito](merit.md)

Il **merito \_ NORMALE** -1

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

> [!Note]  
> Una versione precedente della documentazione ha dichiarato che questo filtro può decodificare "MPEG-2 audio". Il filtro decodifica solo l'audio MPEG-2 compatibile con le versioni precedenti.

 

## <a name="remarks"></a>Commenti

I flussi mono sono sempre decodificati in stereo.

Per i flussi con una configurazione di canale di due o più altoparlanti, il decodificatore esegue una delle operazioni seguenti:

-   Si mescola a sei canali, usando la configurazione comune del altoparlante 5,1.
-   Da downmixes a stereo.

Per selezionare una delle due opzioni, usare l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per impostare la proprietà [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , prima di connettere i pin. In alternativa, quando l'applicazione compila il grafico del filtro, può impostare il tipo di supporto desiderato sul pin di output.

### <a name="aac-decoding"></a>Decodifica AAC

Per AAC, il decodificatore presenta determinati vincoli di formato nell'input AAC compresso. Questi vincoli di formato sono identici a quelli del [**Decodificatore Media Foundation AAC**](../medfound/aac-decoder.md)e sono documentati nella sezione "[**vincoli di formato**](../medfound/aac-decoder.md)".

Il decodificatore DirectShow accetta anche tipi di input diversi rispetto al decodificatore Media Foundation. Il decodificatore DirectShow supporta i tipi di input AAC seguenti:

-   **MEDIASUBTYPE \_ \_AAC1 RAW**: AAC non elaborato, in genere disponibile in AVI o Matroska (. File MKV).
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC in un flusso di trasporto dati audio (ADTS) per lo streaming.
-   **MEDIASUBTYPE \_ MPEG \_ LOAS**: flusso di trasporto con un livello di sincronizzazione (LOAS) e un livello multiplex (latm).

Il decodificatore Media Foundation supporta i tipi di input AAC seguenti:

-   MFAudioFormat \_ AAC (uguale a **MEDIASUBTYPE \_ MPEG \_ HEAAC**) per la riproduzione di file MP4.
-   **MEDIASUBTYPE \_ \_AAC1 non elaborati**.

### <a name="property-sets"></a>Set di proprietà

Il pin di input del decodificatore supporta i set di proprietà seguenti tramite [**IKsPropertySet**](ikspropertyset.md):

-   [**Set di proprietà di protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Set di proprietà di modifica della frequenza**](rate-change-property-set.md).

> [!Note]  
> A partire da Windows 7, il decodificatore supporta la modalità Trick tramite il set di proprietà rate-Change. Supporta le frequenze di riproduzione nell'intervallo \[ 0,501 – 2,0 \] , dove 1,0 è la frequenza di riproduzione normale e 2,0 è il doppio della normale frequenza.

 

### <a name="codec-properties"></a>Proprietà codec

Il pin di input del decodificatore supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Proprietà                                                          | Richiede                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Solo Windows Vista; non supportato in Windows 7 o versioni successive. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Proprietà                                                                          | Richiede      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (vedere la nota 3). | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. Prima di connettere il pin di output del decodificatore, è necessario impostare la proprietà [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) . In caso contrario, la modifica non ha alcun effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, \[ solo app desktop Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sottotipi audio**](audio-subtypes.md)
</dt> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti DVD**](dvd-media-types.md)
</dt> </dl>

 

 
