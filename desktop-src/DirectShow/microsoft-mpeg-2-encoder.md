---
description: Il filtro Microsoft MPEG-2 Encoder codifica audio e video MPEG-2 e multiplex i flussi per generare un flusso di programma MPEG-2 o un flusso di trasporto.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Microsoft MPEG-2 encoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745967"
---
# <a name="microsoft-mpeg-2-encoder"></a>Codificatore Microsoft MPEG-2

Il filtro Microsoft MPEG-2 Encoder codifica audio e video MPEG-2 e multiplex i flussi per generare un flusso di programma MPEG-2 o un flusso di trasporto.

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Informazioni sul filtro

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipi di supporti pin di input

Vedere la sezione Osservazioni

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

Vedere la sezione Osservazioni

Interfacce del PIN di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID filtro

**CLSID \_ CMPEG2EncoderDS** (dichiarata in wmcodecdsp. h)

File eseguibile

msmpeg2enc.dll

[Merito](merit.md)

**il merito non viene \_ \_ \_ utilizzato**

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Commenti

Questo filtro combina la funzionalità di codifica di altri due filtri:

-   [**Codificatore audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)
-   [**Codificatore video Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md)

Ad eccezione di quanto indicato, questo filtro supporta le stesse funzionalità di codifica di questi due codificatori.

Inizialmente il filtro ha un pin di input, che può accettare l'input audio o video. Quando tale PIN è connesso, il filtro crea un secondo pin di input. Se il primo pin di input riceve audio, il secondo pin di input accetta solo video e viceversa. Ogni pin di input supporta gli stessi tipi di supporti del filtro del codificatore corrispondente.

Se è connesso un solo pin di input, il filtro supporta gli stessi tipi di output del codificatore audio o video corrispondente. Se entrambi i pin sono connessi, il filtro supporta i tipi di output seguenti:

-   Audio-oggetto visivo in un flusso di programma MPEG-2
-   Audio-oggetto visivo in un flusso di trasporto MPEG-2

Questi corrispondono ai tipi di output seguenti:

-   **MEDIATYPE \_ Flusso**, **\_ \_ programma MEDIASUBTYPE MPEG2**
-   **MEDIATYPE \_ Flusso**, **\_ \_ trasporto MPEG2 MEDIASUBTYPE**

Questo filtro non può eseguire il multiplexing di flussi codificati in precedenza. I flussi di input devono essere file audio/video non compressi, che vengono codificati dal filtro prima del multiplexing. Il flusso multiplexato è limitato a un solo programma, contenente un massimo di un audio e un flusso video.

### <a name="codec-properties"></a>Proprietà codec

Il filtro supporta le proprietà combinate dei filtri [**MPEG-2 audio encoder**](microsoft-mpeg-2-audio-encoder.md) e [**MPEG-2 video encoder**](microsoft-mpeg-2-video-encoder.md) , con la differenza seguente:

-   La proprietà [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) imposta la velocità in bit media per il flusso video.
-   La proprietà [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) imposta la velocità in bit media per il flusso audio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 
