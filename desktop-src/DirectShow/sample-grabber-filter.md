---
description: Il filtro Grabber di esempio consente di recuperare gli esempi mentre passano attraverso il grafico del filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro Grabber di esempio (qedit. h)
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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325030"
---
# <a name="sample-grabber-filter"></a>Filtro Grabber di esempio

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il filtro Grabber di esempio consente di recuperare gli esempi mentre passano attraverso il grafico del filtro. Si tratta di un filtro di trasformazione con un pin di input e un pin di output. Passa tutti i campioni a valle senza modifiche, quindi è possibile inserirli in un grafico di filtro senza modificare il flusso di dati. L'applicazione può quindi recuperare singoli esempi dal filtro chiamando i metodi sull'interfaccia [**ISampleGrabber**](isamplegrabber.md) .

Se si desidera recuperare esempi senza eseguire il rendering dei dati, connettere il filtro Grabber di esempio al filtro [**renderer null**](null-renderer-filter.md) .



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto.                                                                                                                                    |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | Qualsiasi tipo di supporto. Corrisponde al tipo di supporto di input.                                                                                                          |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_SAMPLEGRABBER CLSID                                                                                                                               |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | Qedit.dll                                                                                                                                          |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Per usare questo filtro, aggiungerlo al grafico filtro e chiamare [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) con il tipo di supporto desiderato. Questo metodo specifica il tipo di supporto per le connessioni al pin di input e di output del filtro. Connettere quindi il filtro ad altri filtri nel grafico.

Se si chiama [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**, il filtro memorizza nel buffer ogni campione che riceve prima di passarlo a valle. Chiamare il metodo [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) per recuperare il contenuto corrente del buffer. In alternativa, è possibile chiamare [**ISampleGrabber:: tocallback**](isamplegrabber-setcallback.md) per fare in modo che il filtro richiami una funzione di callback ogni volta che viene ricevuto un campione.

Il filtro presenta le seguenti limitazioni per i formati video:

-   Non supporta i tipi di video con orientamento dall'alto verso il basso ( **biHeight** negativo).
-   Non supporta la struttura del formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo di formato uguale a **Format \_ VideoInfo2**).
-   Rifiuta qualsiasi tipo di video in cui lo stride della superficie non corrisponde alla larghezza del video.

Di conseguenza, il grabber di esempio non si connetterà al renderer video mixing (VMR) per alcuni tipi di video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti dei servizi di modifica DirectShow](directshow-editing-services-objects.md)
</dt> <dt>

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> </dl>

 

 




