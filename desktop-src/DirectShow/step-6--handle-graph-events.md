---
description: Questo argomento è il passaggio 6 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Passaggio 6: gestire gli eventi del grafo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316317"
---
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="69eb7-103">Passaggio 6: gestire gli eventi del grafo</span><span class="sxs-lookup"><span data-stu-id="69eb7-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="69eb7-104">Questo argomento è il passaggio 6 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="69eb7-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="69eb7-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="69eb7-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="69eb7-106">Quando l'applicazione crea una nuova istanza di Filter Graph Manager, l'applicazione chiama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="69eb7-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="69eb7-107">Questo metodo registra la finestra dell'applicazione per la ricezione di eventi dal grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="69eb7-107">This method registers the application window to receive events from the filter graph.</span></span>


```C++
    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="69eb7-108">Il valore `WM_GRAPH_EVENT` è un messaggio di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="69eb7-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="69eb7-109">Ogni volta che l'applicazione riceve questo messaggio, chiama il `DShowPlayer::HandleGraphEvent` metodo.</span><span class="sxs-lookup"><span data-stu-id="69eb7-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="69eb7-110">Il metodo `DShowPlayer::HandleGraphEvent` esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="69eb7-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="69eb7-111">Chiama [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in un ciclo per ottenere tutti gli eventi in coda.</span><span class="sxs-lookup"><span data-stu-id="69eb7-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="69eb7-112">Richiama una funzione di callback (*pfnOnGraphEvent*).</span><span class="sxs-lookup"><span data-stu-id="69eb7-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="69eb7-113">Chiama [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per liberare i dati associati a ogni evento.</span><span class="sxs-lookup"><span data-stu-id="69eb7-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



<span data-ttu-id="69eb7-114">Nel codice seguente viene illustrata la funzione di callback passata a `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="69eb7-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="69eb7-115">La funzione gestisce il numero minimo di eventi del grafo ([**EC \_ completa**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)e [**EC \_ USERABORT**](ec-userabort.md)). è possibile espandere la funzione per gestire eventi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="69eb7-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="69eb7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69eb7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69eb7-117">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="69eb7-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="69eb7-118">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="69eb7-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="69eb7-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="69eb7-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="69eb7-120">Risposta agli eventi</span><span class="sxs-lookup"><span data-stu-id="69eb7-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



