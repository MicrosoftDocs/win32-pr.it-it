---
description: Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Microsoft MPEG-2 Audio Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584121"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Codificatore audio MPEG-2 Microsoft

Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).

Per codificare e codificare flussi audio/video multiplex, usare il filtro [**Microsoft MPEG-2 Encoder,**](microsoft-mpeg-2-encoder.md) che incapsula le funzioni di questo filtro e del filtro [**Microsoft MPEG-2 Video Encoder.**](microsoft-mpeg-2-video-encoder.md)

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Filtrare le informazioni

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ PCM**

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Flusso,** **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/>

Interfacce pin di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtro CLSID

**CLSID \_ CMPEG2EncoderAudioDS** (dichiarato in wmcodecdsp.h)

File eseguibile

msmpeg2enc.dll

[Merito](merit.md)

**MERITO \_ NON \_ \_ USARE**

[Categoria filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Commenti

MpEG-2 Audio Encoder può produrre i tipi di output seguenti:

-   Flusso elementare audio
-   Audio in un flusso di programma MPEG-2
-   Audio in un flusso di trasporto MPEG-2

Supporta le estensioni mpeg-1 livelli I e II e MPEG-2 a bassa frequenza di campionamento (LSF)

I campioni di input devono avere 16 bit per campione, con una frequenza di campionamento audio di 48, 44,1, 32, 22,05 o 16 KHz. Il codificatore non può ricampionare il flusso audio. l'audio codificato ha la stessa frequenza di campionamento dell'input.

Gli esempi di input devono essere mono o stereo. L'audio codificato ha il numero di canali come input.

### <a name="limitations"></a>Limitazioni

Il codificatore non supporta quanto segue:

-   Flusso di bit audio MPEG livello III.
-   Bitstream di estensione multicanale MPEG-2.
-   Flusso di bit MPEG-4 AAC.
-   Flusso di bit MPEG-2 non compatibile con le versioni precedenti (NBC).
-   Generazione di pacchetti PES (Packetized Elementary Stream).
-   Codifica digitale Dolby.

### <a name="codec-properties"></a>Proprietà codec

Il filtro supporta le proprietà seguenti tramite [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> In una versione precedente della documentazione sono elencate erroneamente alcune proprietà aggiuntive non supportate.

 

Per compatibilità con le versioni precedenti, il filtro supporta la proprietà seguente tramite **l'interfaccia IEncoderAPI:**



| Proprietà                 | Descrizione                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **VELOCITÀ IN BIT ENCAPIPARAM \_** | Equivale a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

È consigliabile impostare le proprietà nell'ordine seguente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Impostare le proprietà rimanenti in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
