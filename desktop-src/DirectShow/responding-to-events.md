---
description: Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Risposta agli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521401"
---
# <a name="responding-to-events"></a><span data-ttu-id="48242-103">Risposta agli eventi</span><span class="sxs-lookup"><span data-stu-id="48242-103">Responding to Events</span></span>

<span data-ttu-id="48242-104">Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="48242-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="48242-105">Funzionamento della notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="48242-105">How Event Notification Works</span></span>

<span data-ttu-id="48242-106">Durante l'esecuzione di un'applicazione DirectShow, è possibile che si verifichino eventi nel grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="48242-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="48242-107">Ad esempio, un filtro potrebbe rilevare un errore di streaming.</span><span class="sxs-lookup"><span data-stu-id="48242-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="48242-108">I filtri inviano avvisi al gestore del grafico dei filtri inviando eventi, che sono costituiti da un codice evento e due parametri di evento.</span><span class="sxs-lookup"><span data-stu-id="48242-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="48242-109">Il codice evento indica il tipo di evento e i parametri dell'evento forniscono informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="48242-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="48242-110">Il significato dei parametri dipende dal codice evento.</span><span class="sxs-lookup"><span data-stu-id="48242-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="48242-111">Per un elenco completo dei codici evento, vedere [codici di notifica degli eventi](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="48242-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="48242-112">Alcuni eventi vengono gestiti automaticamente da Filter Graph Manager, senza che l'applicazione venga inviata una notifica.</span><span class="sxs-lookup"><span data-stu-id="48242-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="48242-113">Altri eventi vengono inseriti in una coda per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48242-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="48242-114">A seconda dell'applicazione, è possibile che sia necessario gestire vari eventi.</span><span class="sxs-lookup"><span data-stu-id="48242-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="48242-115">Questo articolo è incentrato su tre eventi molto comuni:</span><span class="sxs-lookup"><span data-stu-id="48242-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="48242-116">L'evento [**EC \_ complete**](ec-complete.md) indica che la riproduzione è stata completata normalmente.</span><span class="sxs-lookup"><span data-stu-id="48242-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="48242-117">L'evento [**EC \_ USERABORT**](ec-userabort.md) indica che l'utente ha interrotto la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="48242-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="48242-118">I renderer video inviano questo evento se l'utente chiude la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="48242-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="48242-119">L'evento [**EC \_ ERRORABORT**](ec-errorabort.md) indica che un errore ha causato l'interruzione della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="48242-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="48242-120">Uso della notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="48242-120">Using Event Notification</span></span>

<span data-ttu-id="48242-121">Un'applicazione può indicare a Filter Graph Manager di inviare un messaggio di Windows a una finestra specificata ogni volta che si verifica un nuovo evento.</span><span class="sxs-lookup"><span data-stu-id="48242-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="48242-122">Ciò consente all'applicazione di rispondere all'interno del ciclo di messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="48242-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="48242-123">In primo luogo, definire il messaggio che verrà inviato alla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48242-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="48242-124">Le applicazioni possono usare i numeri dei messaggi nell'intervallo dall' \_ app WM tramite 0xBFFF come messaggi privati:</span><span class="sxs-lookup"><span data-stu-id="48242-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="48242-125">Successivamente, eseguire una query su Filter Graph Manager per l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) e chiamare il metodo [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :</span><span class="sxs-lookup"><span data-stu-id="48242-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="48242-126">Questo metodo definisce la finestra specificata (g \_ HWND) come destinatario del messaggio.</span><span class="sxs-lookup"><span data-stu-id="48242-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="48242-127">Chiamare il metodo dopo aver creato il grafico del filtro, ma prima di eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="48242-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="48242-128">WM \_ GRAPHNOTIFY è un normale messaggio di Windows.</span><span class="sxs-lookup"><span data-stu-id="48242-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="48242-129">Ogni volta che il gestore del grafico dei filtri inserisce un nuovo evento nella coda degli eventi, invia un \_ messaggio GRAPHNOTIFY WM alla finestra dell'applicazione designata.</span><span class="sxs-lookup"><span data-stu-id="48242-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="48242-130">Il parametro *lParam* del messaggio è uguale al terzo parametro in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="48242-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="48242-131">Questo parametro consente di inviare i dati dell'istanza con il messaggio.</span><span class="sxs-lookup"><span data-stu-id="48242-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="48242-132">Il parametro *wParam* del messaggio della finestra è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="48242-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="48242-133">Nella funzione **WindowProc** dell'applicazione aggiungere un'istruzione case per il \_ messaggio WM GRAPHNOTIFY:</span><span class="sxs-lookup"><span data-stu-id="48242-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="48242-134">Nella funzione del gestore eventi chiamare il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per recuperare gli eventi dalla coda:</span><span class="sxs-lookup"><span data-stu-id="48242-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="48242-135">Il metodo [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) Recupera il codice evento e i due parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="48242-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="48242-136">Il quarto parametro **GetEvent** specifica l'intervallo di tempo di attesa di un evento, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="48242-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="48242-137">Poiché l'applicazione chiama questo metodo in risposta a un \_ messaggio WM GRAPHNOTIFY, l'evento è già in coda.</span><span class="sxs-lookup"><span data-stu-id="48242-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="48242-138">Pertanto, il valore di timeout viene impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="48242-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="48242-139">La notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, quindi la coda potrebbe avere più di un evento nel momento in cui l'applicazione risponde al messaggio.</span><span class="sxs-lookup"><span data-stu-id="48242-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="48242-140">Inoltre, il gestore del grafo del filtro può rimuovere determinati eventi dalla coda, se diventano non validi.</span><span class="sxs-lookup"><span data-stu-id="48242-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="48242-141">Pertanto, è necessario chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) fino a quando non viene restituito un codice di errore, che indica che la coda è vuota.</span><span class="sxs-lookup"><span data-stu-id="48242-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="48242-142">In questo esempio, l'applicazione risponde a [**EC \_ complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)e [**EC \_ ERRORABORT**](ec-errorabort.md) richiamando la funzione di pulizia definita dall'applicazione, che causa la chiusura normale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48242-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="48242-143">Nell'esempio vengono ignorati i due parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="48242-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="48242-144">Dopo aver recuperato un evento, chiamare [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) in tutte le risorse gratuite associate ai parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="48242-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="48242-145">Si noti che un evento [**EC \_ complete**](ec-complete.md) non determina l'arresto del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="48242-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="48242-146">L'applicazione può arrestare o sospendere il grafo.</span><span class="sxs-lookup"><span data-stu-id="48242-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="48242-147">Se si arresta il grafo, i filtri rilasciano tutte le risorse che contengono.</span><span class="sxs-lookup"><span data-stu-id="48242-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="48242-148">Se si sospende il grafo, i filtri continuano a mantenere le risorse.</span><span class="sxs-lookup"><span data-stu-id="48242-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="48242-149">Inoltre, quando un renderer video viene sospeso, viene visualizzata un'immagine statica del frame più recente.</span><span class="sxs-lookup"><span data-stu-id="48242-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="48242-150">Prima di rilasciare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annullare la notifica degli eventi chiamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un handle di finestra **null** :</span><span class="sxs-lookup"><span data-stu-id="48242-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="48242-151">Nel gestore di \_ messaggi WM GRAPHNOTIFY controllare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) prima di chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span><span class="sxs-lookup"><span data-stu-id="48242-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="48242-152">In questo modo si evita un possibile errore che può verificarsi se l'applicazione riceve la notifica degli eventi dopo aver rilasciato il puntatore.</span><span class="sxs-lookup"><span data-stu-id="48242-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48242-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48242-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48242-154">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="48242-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="48242-155">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="48242-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



