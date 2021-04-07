---
description: Scaricamento dei dati
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Scaricamento dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745634"
---
# <a name="flushing-data"></a><span data-ttu-id="e1c7d-103">Scaricamento dei dati</span><span class="sxs-lookup"><span data-stu-id="e1c7d-103">Flushing Data</span></span>

<span data-ttu-id="e1c7d-104">Nello pseudocodice seguente viene illustrato come implementare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :</span><span class="sxs-lookup"><span data-stu-id="e1c7d-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



<span data-ttu-id="e1c7d-105">Quando viene avviato lo scaricamento, il metodo **BeginFlush** accetta il blocco del filtro, che serializza la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="e1c7d-106">Non è ancora possibile eseguire il blocco di streaming perché lo svuotamento avviene nel thread dell'applicazione e il thread di streaming potrebbe trovarsi al centro di una chiamata di **ricezione** .</span><span class="sxs-lookup"><span data-stu-id="e1c7d-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="e1c7d-107">Il PIN deve garantire che la **ricezione** non venga bloccata e che tutte le chiamate successive a **Receive** avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="e1c7d-108">Il metodo [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) imposta un flag interno, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md).</span><span class="sxs-lookup"><span data-stu-id="e1c7d-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="e1c7d-109">Quando il flag è **true**, il metodo **Receive** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="e1c7d-110">Grazie alla chiamata a downstream di **BeginFlush** , il PIN garantisce che tutti i filtri downstream rilascino gli esempi e restituiscano le chiamate di **ricezione** .</span><span class="sxs-lookup"><span data-stu-id="e1c7d-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="e1c7d-111">Questo garantisce a sua volta che il pin di input non è bloccato in attesa di **GetBuffer** o **Receive**.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="e1c7d-112">Se il metodo di **ricezione** del PIN è in attesa di un evento, ad esempio per ottenere le risorse, il metodo **BeginFlush** deve forzare l'attesa per terminare impostando l'evento.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="e1c7d-113">A questo punto, viene garantita la restituzione del metodo **Receive** e il flag **m \_ bFlushing** impedisce a nuove chiamate **Receive** di eseguire qualsiasi operazione.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="e1c7d-114">Per alcuni filtri, questa operazione deve essere eseguita da tutti i **BeginFlush** .</span><span class="sxs-lookup"><span data-stu-id="e1c7d-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="e1c7d-115">Il metodo **EndFlush** segnalerà al filtro che può iniziare a ricevere nuovamente gli esempi.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="e1c7d-116">Altri filtri potrebbero dover usare variabili o risorse in **BeginFlush** che vengono usate anche nella **ricezione**.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="e1c7d-117">In tal caso, il filtro deve prima tenere il blocco di streaming.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="e1c7d-118">Assicurarsi di non eseguire questa operazione prima di uno dei passaggi precedenti, perché potrebbe verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="e1c7d-119">Il metodo **EndFlush** include il blocco del filtro e propaga la chiamata downstream:</span><span class="sxs-lookup"><span data-stu-id="e1c7d-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="e1c7d-120">Il metodo [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) Reimposta il flag **m \_ bFlushing** su **false**, che consente al metodo **Receive** di iniziare a ricevere nuovamente gli esempi.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="e1c7d-121">Questo deve essere l'ultimo passaggio di **EndFlush**, perché il PIN non deve ricevere alcun campione fino al completamento dello scaricamento e alla notifica di tutti i filtri downstream.</span><span class="sxs-lookup"><span data-stu-id="e1c7d-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c7d-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1c7d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c7d-123">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="e1c7d-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



