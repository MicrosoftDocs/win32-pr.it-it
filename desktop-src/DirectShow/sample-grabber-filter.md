---
description: Il filtro Sample Grabber consente di recuperare gli esempi mentre passano attraverso il grafico dei filtri.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro Grabber di esempio (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909669"
---
# <a name="sample-grabber-filter"></a>Filtro Grabber di esempio

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il filtro Sample Grabber consente di recuperare gli esempi mentre passano attraverso il grafico dei filtri. Si tratta di un filtro di trasformazione con un pin di input e un pin di output. Passa tutti i campioni a valle senza modifiche, quindi è possibile inserirli in un grafico di filtro senza modificare il flusso di dati. L'applicazione può quindi recuperare singoli esempi dal filtro chiamando i metodi [**nell'interfaccia ISampleGrabber.**](isamplegrabber.md)

Per recuperare gli esempi senza eseguire il rendering dei dati, connettere il filtro Sample Grabber al filtro [**Renderer**](null-renderer-filter.md) Null.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto.                                                                                                                                    |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | Qualsiasi tipo di supporto. Corrisponde al tipo di supporto di input.                                                                                                          |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | Qedit.dll                                                                                                                                          |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Per usare questo filtro, aggiungerlo al grafico dei filtri e chiamare [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) con il tipo di supporto desiderato. Questo metodo specifica il tipo di supporto per le connessioni di input e pin di output del filtro. Connettere quindi il filtro ad altri filtri nel grafico.

Se si chiama [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **TRUE,** il filtro bufferizza ogni campione ricevuto prima di passarlo a valle. Chiamare il [**metodo ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) per recuperare il contenuto corrente del buffer. In alternativa, è possibile chiamare [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) per fare in modo che il filtro chiami una funzione di callback ogni volta che riceve un esempio.

Il filtro presenta le limitazioni seguenti per i formati video:

-   Non supporta i tipi di video con orientamento dall'alto verso il basso **(biHeight negativo).**
-   Non supporta la struttura di [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo di formato uguale a **FORMAT \_ VideoInfo2**).
-   Rifiuta qualsiasi tipo di video in cui lo stride della superficie non corrisponde alla larghezza del video.

Di conseguenza, Sample Grabber non si connetterà al renderer di combinazione di video per alcuni tipi di video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Editing Services Objects](directshow-editing-services-objects.md)
</dt> <dt>

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> </dl>

 

 




