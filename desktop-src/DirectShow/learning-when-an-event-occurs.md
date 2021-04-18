---
description: Apprendimento quando si verifica un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Apprendimento quando si verifica un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522066"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="21da7-103">Apprendimento quando si verifica un evento</span><span class="sxs-lookup"><span data-stu-id="21da7-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="21da7-104">Per elaborare gli eventi DirectShow, un'applicazione necessita di un modo per individuare quando gli eventi sono in attesa nella coda.</span><span class="sxs-lookup"><span data-stu-id="21da7-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="21da7-105">Per eseguire questa operazione, il gestore del grafo del filtro offre due modi:</span><span class="sxs-lookup"><span data-stu-id="21da7-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="21da7-106">**Notifica finestra:** Filter Graph Manager invia un messaggio di Windows definito dall'utente a una finestra dell'applicazione ogni volta che viene eseguito un nuovo evento.</span><span class="sxs-lookup"><span data-stu-id="21da7-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="21da7-107">**Segnalazione evento:** Filter Graph Manager segnala un evento Windows se sono presenti eventi DirectShow nella coda e Reimposta l'evento se la coda è vuota.</span><span class="sxs-lookup"><span data-stu-id="21da7-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="21da7-108">Un'applicazione può utilizzare una delle due tecniche.</span><span class="sxs-lookup"><span data-stu-id="21da7-108">An application can use either technique.</span></span> <span data-ttu-id="21da7-109">La notifica della finestra è in genere più semplice.</span><span class="sxs-lookup"><span data-stu-id="21da7-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="21da7-110">**Notifica finestra**</span><span class="sxs-lookup"><span data-stu-id="21da7-110">**Window Notification**</span></span>

<span data-ttu-id="21da7-111">Per impostare la notifica della finestra, chiamare il metodo [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) e specificare un messaggio privato.</span><span class="sxs-lookup"><span data-stu-id="21da7-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="21da7-112">Le applicazioni possono usare i numeri dei messaggi nell'intervallo dall' \_ app WM tramite 0xBFFF come messaggi privati.</span><span class="sxs-lookup"><span data-stu-id="21da7-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="21da7-113">Ogni volta che il gestore del grafico dei filtri inserisce una nuova notifica degli eventi nella coda, invia questo messaggio alla finestra designata.</span><span class="sxs-lookup"><span data-stu-id="21da7-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="21da7-114">L'applicazione risponde al messaggio dall'interno del ciclo di messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="21da7-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="21da7-115">Nell'esempio di codice riportato di seguito viene illustrato come impostare la finestra di notifica.</span><span class="sxs-lookup"><span data-stu-id="21da7-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="21da7-116">Il messaggio è un normale messaggio di Windows e viene pubblicato separatamente dalla coda di notifiche degli eventi DirectShow.</span><span class="sxs-lookup"><span data-stu-id="21da7-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="21da7-117">Il vantaggio di questo approccio è che la maggior parte delle applicazioni implementa già un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="21da7-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="21da7-118">Pertanto, è possibile incorporare la gestione degli eventi DirectShow senza molto lavoro aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="21da7-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="21da7-119">Nell'esempio di codice seguente viene illustrata la modalità di risposta al messaggio di notifica.</span><span class="sxs-lookup"><span data-stu-id="21da7-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="21da7-120">Per un esempio completo, vedere [rispondere agli eventi](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="21da7-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="21da7-121">Poiché la notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, la coda potrebbe contenere più di un evento nel momento in cui l'applicazione risponde al messaggio.</span><span class="sxs-lookup"><span data-stu-id="21da7-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="21da7-122">Inoltre, gli eventi possono a volte essere cancellati dalla coda se diventano non validi.</span><span class="sxs-lookup"><span data-stu-id="21da7-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="21da7-123">Nel codice di gestione degli eventi, quindi, chiamare [**IAMMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) fino a quando non viene restituito un codice di errore, a indicare che la coda è vuota.</span><span class="sxs-lookup"><span data-stu-id="21da7-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="21da7-124">Prima di rilasciare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annullare la notifica degli eventi chiamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="21da7-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="21da7-125">Nel codice di elaborazione degli eventi controllare se il puntatore **IMediaEventEx** è valido prima di chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="21da7-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="21da7-126">Questa procedura impedisce un possibile errore, in cui l'applicazione riceve la notifica degli eventi dopo aver rilasciato il puntatore **IMediaEventEx** .</span><span class="sxs-lookup"><span data-stu-id="21da7-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="21da7-127">**Segnalazione di eventi**</span><span class="sxs-lookup"><span data-stu-id="21da7-127">**Event Signaling**</span></span>

<span data-ttu-id="21da7-128">Filter Graph Manager mantiene un evento di reimpostazione manuale che riflette lo stato della coda degli eventi.</span><span class="sxs-lookup"><span data-stu-id="21da7-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="21da7-129">Se la coda contiene notifiche di eventi in sospeso, il gestore del grafico del filtro segnala l'evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="21da7-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="21da7-130">Se la coda è vuota, una chiamata al metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) Reimposta l'evento.</span><span class="sxs-lookup"><span data-stu-id="21da7-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="21da7-131">Un'applicazione può utilizzare questo evento per determinare lo stato della coda.</span><span class="sxs-lookup"><span data-stu-id="21da7-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="21da7-132">La terminologia può creare confusione.</span><span class="sxs-lookup"><span data-stu-id="21da7-132">The terminology can be confusing here.</span></span> <span data-ttu-id="21da7-133">L'evento di reimpostazione manuale è il tipo di evento creato dalla funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) di Windows. non ha nulla a che fare con gli eventi definiti da DirectShow.</span><span class="sxs-lookup"><span data-stu-id="21da7-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="21da7-134">Chiamare il metodo [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) per ottenere un handle per l'evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="21da7-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="21da7-135">Attendere che l'evento venga segnalato chiamando una funzione come [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="21da7-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="21da7-136">Una volta segnalato l'evento, chiamare [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere l'evento DirectShow.</span><span class="sxs-lookup"><span data-stu-id="21da7-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="21da7-137">Il seguente esempio di codice illustra questo approccio.</span><span class="sxs-lookup"><span data-stu-id="21da7-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="21da7-138">Ottiene l'handle dell'evento, quindi attende in intervalli di 100 millisecondi che l'evento venga segnalato.</span><span class="sxs-lookup"><span data-stu-id="21da7-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="21da7-139">Se l'evento viene segnalato, chiama **GetEvent** e stampa il codice evento e i parametri dell'evento nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="21da7-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="21da7-140">Il ciclo termina quando si verifica l'evento di [**\_ completamento dell'EC**](ec-complete.md) , a indicare che la riproduzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="21da7-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="21da7-141">Poiché il grafico di filtro imposta o reimposta automaticamente l'evento quando appropriato, l'applicazione non deve eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="21da7-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="21da7-142">Inoltre, quando si rilascia il grafico del filtro, il grafico di filtro chiude l'handle di evento, quindi non usare l'handle di evento dopo tale punto.</span><span class="sxs-lookup"><span data-stu-id="21da7-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
