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
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="73568-103">Gestione degli eventi di ridisegno in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="73568-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="73568-104">Se si compila un grafico di acquisizione video senza usare l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e si visualizza in anteprima il video usando il filtro renderer video precedente, è necessario eseguire l'override della gestione predefinita per gli eventi di [**\_ ridisegno EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="73568-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="73568-105">Eseguire una query su Filter Graph Manager per l'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chiamare il metodo [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il valore EC \_ Repaint:</span><span class="sxs-lookup"><span data-stu-id="73568-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="73568-106">In questo modo si evita un possibile errore che può danneggiare il file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="73568-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="73568-107">Se l'utente copre e individua la finestra di anteprima, il filtro renderer video riceve un messaggio di \_ disegno WM.</span><span class="sxs-lookup"><span data-stu-id="73568-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="73568-108">Per impostazione predefinita, il renderer video richiede un nuovo frame e il gestore del grafo del filtro sospende il grafico per individuare un altro frame video.</span><span class="sxs-lookup"><span data-stu-id="73568-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="73568-109">Se ciò si verifica quando il grafo scrive un file, il file verrà danneggiato.</span><span class="sxs-lookup"><span data-stu-id="73568-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="73568-110">L'override del comportamento di \_ ridisegno EC predefinito impedisce al renderer di richiedere un nuovo frame.</span><span class="sxs-lookup"><span data-stu-id="73568-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="73568-111">Non è necessario eseguire questo passaggio se si usa l'interfaccia **ICaptureGraphBuilder2** , perché il generatore del grafico di acquisizione lo esegue automaticamente.</span><span class="sxs-lookup"><span data-stu-id="73568-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="73568-112">Inoltre, non è necessario se si usa il renderer video mixing (VMR) per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="73568-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="73568-113">Per VMR è sempre disponibile il frame più recente, quindi non vengono inviati \_ gli eventi di ridisegno EC.</span><span class="sxs-lookup"><span data-stu-id="73568-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73568-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73568-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73568-115">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="73568-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="73568-116">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="73568-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



