---
description: Gestione degli eventi di ridisegno in acquisizione video
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Gestione degli eventi di ridisegno in acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965818"
---
# <a name="handling-repaint-events-in-video-capture"></a>Gestione degli eventi di ridisegno in acquisizione video

Se si compila un grafico di acquisizione video senza usare l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e si visualizza in anteprima il video usando il filtro renderer video precedente, è necessario eseguire l'override della gestione predefinita per gli eventi di [**\_ ridisegno EC**](ec-repaint.md) . Eseguire una query su Filter Graph Manager per l'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chiamare il metodo [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il valore EC \_ Repaint:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



In questo modo si evita un possibile errore che può danneggiare il file di acquisizione. Se l'utente copre e individua la finestra di anteprima, il filtro renderer video riceve un messaggio di \_ disegno WM. Per impostazione predefinita, il renderer video richiede un nuovo frame e il gestore del grafo del filtro sospende il grafico per individuare un altro frame video. Se ciò si verifica quando il grafo scrive un file, il file verrà danneggiato. L'override del comportamento di \_ ridisegno EC predefinito impedisce al renderer di richiedere un nuovo frame.

Non è necessario eseguire questo passaggio se si usa l'interfaccia **ICaptureGraphBuilder2** , perché il generatore del grafico di acquisizione lo esegue automaticamente. Inoltre, non è necessario se si usa il renderer video mixing (VMR) per l'anteprima. Per VMR è sempre disponibile il frame più recente, quindi non vengono inviati \_ gli eventi di ridisegno EC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



