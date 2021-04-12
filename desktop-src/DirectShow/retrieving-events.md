---
description: Recupero di eventi
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recupero di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401047"
---
# <a name="retrieving-events"></a><span data-ttu-id="a0ebc-103">Recupero di eventi</span><span class="sxs-lookup"><span data-stu-id="a0ebc-103">Retrieving Events</span></span>

<span data-ttu-id="a0ebc-104">Il gestore del grafo del filtro espone tre interfacce che supportano la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="a0ebc-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contiene il metodo per i filtri per la pubblicazione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="a0ebc-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contiene metodi che consentono alle applicazioni di recuperare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="a0ebc-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) eredita da ed estende l'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="a0ebc-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="a0ebc-108">Filtra le notifiche degli eventi post chiamando il metodo [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="a0ebc-109">Una notifica degli eventi è costituita da un codice evento, che definisce il tipo di evento e due parametri che forniscono informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="a0ebc-110">A seconda del codice evento, i parametri possono contenere puntatori, codici restituiti, tempi di riferimento o altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="a0ebc-111">Per un elenco completo dei parametri e dei codici evento, vedere [codici di notifica degli eventi](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a0ebc-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="a0ebc-112">Per recuperare un evento dalla coda, l'applicazione chiama il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="a0ebc-113">Questo metodo si blocca fino a quando non si verifica un evento da restituire o fino a quando non trascorre un intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="a0ebc-114">Supponendo che sia presente un evento in coda, il metodo restituisce con il codice evento e i due parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="a0ebc-115">Dopo la chiamata a **GetEvent**, un'applicazione deve sempre chiamare il metodo [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per rilasciare tutte le risorse associate ai parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="a0ebc-116">Un parametro, ad esempio, può essere un valore **BSTR** allocato dal grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="a0ebc-117">Nell'esempio di codice seguente viene illustrato come recuperare gli eventi dalla coda.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="a0ebc-118">Per eseguire l'override della gestione predefinita di Filter Graph Manager per un evento, chiamare il metodo [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il codice evento come parametro.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="a0ebc-119">È possibile ripristinare la gestione predefinita chiamando il metodo [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) .</span><span class="sxs-lookup"><span data-stu-id="a0ebc-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="a0ebc-120">Se il grafico del filtro non esegue alcuna gestione predefinita per il codice evento specificato, la chiamata a questi metodi non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="a0ebc-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0ebc-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0ebc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0ebc-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0ebc-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



