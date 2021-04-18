---
description: Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificatore audio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303991"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Codificatore audio Microsoft MPEG-2

Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).

Per codificare i flussi audio/video multiplex, usare il filtro [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) , che incapsula le funzioni di questo filtro e del filtro [**codificatore video Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Informazioni sul filtro

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Audio**, **\_ \_ audio MPEG2 MEDIASUBTYPE**<br/> **MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ \_ audio MPEG2**<br/> **MEDIATYPE \_ Flusso**, **\_ \_ programma MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Flusso**, **\_ \_ trasporto MPEG2 MEDIASUBTYPE**<br/>

Interfacce del PIN di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID filtro

**CLSID \_ CMPEG2EncoderAudioDS** (dichiarata in wmcodecdsp. h)

File eseguibile

msmpeg2enc.dll

[Merito](merit.md)

**il merito non viene \_ \_ \_ utilizzato**

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Commenti

Il codificatore audio MPEG-2 può produrre i tipi di output seguenti:

-   Flusso audio elementare
-   Audio in un flusso di programma MPEG-2
-   Audio in un flusso di trasporto MPEG-2

Supporta le estensioni MPEG-1 Layer I e II e MPEG-2 Low Sampling Frequency (LSF)

Gli esempi di input devono essere a 16 bit per campione, con una frequenza di campionamento audio di 48, 44,1, 32, 22,05 o 16 KHz. Il codificatore non può ricampionare il flusso audio; l'audio codificato ha la stessa frequenza di campionamento dell'input.

Gli esempi di input devono essere mono o stereo. L'audio codificato ha il numero di canali come input.

### <a name="limitations"></a>Limitazioni

Il codificatore non supporta quanto segue:

-   Bitstream audio MPEG Layer III.
-   Bitstream di estensione multicanale MPEG-2.
-   Bitstream MPEG-4 AAC.
-   Bitstream MPEG-2 non compatibili con le versioni precedenti (NBC).
-   Generazione di pacchetti di flusso elementare (PES) in pacchetto.
-   Codifica Dolby Digital.

### <a name="codec-properties"></a>Proprietà codec

Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

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
> Una versione precedente della documentazione elenca erroneamente alcune proprietà aggiuntive che non sono supportate.

 

Per compatibilità con le versioni precedenti, il filtro supporta la seguente proprietà tramite l'interfaccia **IEncoderAPI** :



| Proprietà                 | Descrizione                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **\_velocità in bit ENCAPIPARAM** | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

È consigliabile impostare le proprietà nell'ordine seguente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Impostare le proprietà rimanenti in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti di Demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
