---
description: Gestione degli eventi di ridisegno nell'acquisizione video
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Gestione degli eventi di ridisegno nell'acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433a9897c7c69119eb54d088aff2d22536e20ae43760cc6b4c9430f9a44f6814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999760"
---
# <a name="handling-repaint-events-in-video-capture"></a>Gestione degli eventi di ridisegno nell'acquisizione video

Se si crea un grafo di acquisizione video senza usare l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e si visualizza in anteprima il video usando il filtro del renderer video precedente, è necessario eseguire l'override della gestione predefinita per gli eventi [**EC \_ REPAINT.**](ec-repaint.md) Eseguire una query su Filter Graph Manager per l'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chiamare il metodo [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il valore EC \_ REPAINT:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



In questo modo si evita un possibile errore che può danneggiare il file di acquisizione. Se l'utente copre e individua la finestra di anteprima, il filtro renderer video riceve un messaggio WM \_ PAINT. Per impostazione predefinita, il renderer video richiede un nuovo fotogramma e Filter Graph Manager sospende il grafico per creare un altro fotogramma video. Se ciò si verifica durante la scrittura di un file da parte del grafo, il file verrà danneggiato. L'override del comportamento EC \_ REPAINT predefinito impedisce al renderer di richiedere un nuovo frame.

Non è necessario eseguire questo passaggio se si usa **l'interfaccia ICaptureGraphBuilder2,** perché Capture Graph Builder esegue automaticamente questa operazione. Inoltre, non è necessario se si usa il renderer di combinazione di video (VMR) per l'anteprima. Il vmr ha sempre il frame più recente disponibile, quindi non invia eventi EC \_ REPAINT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati sull'acquisizione](advanced-capture-topics.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



