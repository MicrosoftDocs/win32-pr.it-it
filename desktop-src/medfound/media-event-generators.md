---
description: Generatori di eventi multimediali
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Generatori di eventi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320773"
---
# <a name="media-event-generators"></a><span data-ttu-id="b86b6-103">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="b86b6-103">Media Event Generators</span></span>

<span data-ttu-id="b86b6-104">Media Foundation consente agli oggetti di inviare eventi in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="b86b6-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="b86b6-105">Un oggetto può usare gli eventi per segnalare il completamento di un metodo asincrono o per notificare all'applicazione una modifica nello stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b86b6-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="b86b6-106">Se un oggetto invia eventi, espone l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b86b6-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="b86b6-107">Ogni volta che l'oggetto invia un nuovo evento, l'evento viene inserito in una coda.</span><span class="sxs-lookup"><span data-stu-id="b86b6-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="b86b6-108">L'applicazione può richiedere l'evento successivo dalla coda chiamando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b86b6-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="b86b6-109">**IMFMediaEventGenerator:: GetEvent**</span><span class="sxs-lookup"><span data-stu-id="b86b6-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="b86b6-110">**IMFMediaEventGenerator::BeginGetEvent**</span><span class="sxs-lookup"><span data-stu-id="b86b6-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="b86b6-111">Il metodo [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) è sincrono.</span><span class="sxs-lookup"><span data-stu-id="b86b6-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="b86b6-112">Se un evento è già presente nella coda, il metodo restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="b86b6-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="b86b6-113">Se nella coda non è presente alcun evento, il metodo ha esito negativo immediatamente oppure si blocca fino a quando l'evento successivo non viene accodato, a seconda del flag passato a **GetEvent**.</span><span class="sxs-lookup"><span data-stu-id="b86b6-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="b86b6-114">Il metodo [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) è asincrono, pertanto non viene mai bloccato.</span><span class="sxs-lookup"><span data-stu-id="b86b6-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="b86b6-115">Questo metodo accetta un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , che deve essere implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b86b6-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="b86b6-116">Quando viene richiamato il callback, l'applicazione chiama [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ottenere l'evento dalla coda.</span><span class="sxs-lookup"><span data-stu-id="b86b6-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="b86b6-117">Per altre informazioni su **IMFAsyncCallback**, vedere [metodi di callback asincroni](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b86b6-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="b86b6-118">Gli eventi sono rappresentati dall'interfaccia [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="b86b6-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="b86b6-119">Questa interfaccia presenta i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b86b6-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="b86b6-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Recupera il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="b86b6-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="b86b6-121">Il tipo di evento indica che cosa è successo ad attivare l'evento.</span><span class="sxs-lookup"><span data-stu-id="b86b6-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="b86b6-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Recupera un valore **HRESULT** che indica se l'operazione che ha attivato l'evento è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b86b6-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="b86b6-123">Se un'operazione ha esito negativo in modo asincrono, **GetStatus** restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="b86b6-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="b86b6-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Recupera un **PROPVARIANT** che contiene i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b86b6-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="b86b6-125">I dati dell'evento dipendono dal tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="b86b6-125">The event data depends on the event type.</span></span> <span data-ttu-id="b86b6-126">Alcuni eventi non contengono dati.</span><span class="sxs-lookup"><span data-stu-id="b86b6-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="b86b6-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Recupera un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="b86b6-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="b86b6-128">Questo metodo si applica all' [evento MEExtendedType](meextendedtype.md)e fornisce un modo per definire eventi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b86b6-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="b86b6-129">L'interfaccia [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) eredita anche l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="b86b6-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="b86b6-130">Alcuni eventi contengono informazioni aggiuntive come attributi.</span><span class="sxs-lookup"><span data-stu-id="b86b6-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="b86b6-131">Per un elenco dei tipi di evento e i relativi dati e attributi associati, vedere [eventi Media Foundation](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="b86b6-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="b86b6-132">Implementazione di IMFMediaEventGenerator</span><span class="sxs-lookup"><span data-stu-id="b86b6-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="b86b6-133">Se si sta scrivendo un componente plug-in per Media Foundation, ad esempio un'origine multimediale personalizzata o un sink multimediale, potrebbe essere necessario implementare [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span><span class="sxs-lookup"><span data-stu-id="b86b6-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="b86b6-134">Per semplificare questa operazione, Media Foundation fornisce un oggetto helper che implementa una coda degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b86b6-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="b86b6-135">Creare la coda degli eventi chiamando la funzione [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="b86b6-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="b86b6-136">La coda degli eventi espone l'interfaccia [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="b86b6-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="b86b6-137">Nell'implementazione dell'oggetto dei metodi **IMFMediaEventGenerator** , chiamare il metodo corrispondente nella coda degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b86b6-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="b86b6-138">L'oggetto coda di eventi è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b86b6-138">The event queue object is thread safe.</span></span> <span data-ttu-id="b86b6-139">Non mantenere mai lo stesso oggetto sezione critica quando si chiamano [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) e [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), perché **GetEvent** potrebbe bloccarsi per un tempo indefinito in attesa di [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span><span class="sxs-lookup"><span data-stu-id="b86b6-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="b86b6-140">Se si tiene la stessa sezione critica per entrambi i metodi, verrà generato un deadlock.</span><span class="sxs-lookup"><span data-stu-id="b86b6-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="b86b6-141">Prima di rilasciare la coda degli eventi, chiamare [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) per rilasciare le risorse detenute dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b86b6-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="b86b6-142">Quando l'oggetto deve generare un evento, chiamare uno dei metodi seguenti nella coda degli eventi:</span><span class="sxs-lookup"><span data-stu-id="b86b6-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="b86b6-143">**IMFMediaEventQueue::QueueEvent**</span><span class="sxs-lookup"><span data-stu-id="b86b6-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="b86b6-144">**IMFMediaEventQueue::QueueEventParamVar**</span><span class="sxs-lookup"><span data-stu-id="b86b6-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="b86b6-145">**IMFMediaEventQueue::QueueEventParamUnk**</span><span class="sxs-lookup"><span data-stu-id="b86b6-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="b86b6-146">Questi metodi inseriscono un nuovo evento nella coda e segnalano qualsiasi chiamante in attesa dell'evento successivo.</span><span class="sxs-lookup"><span data-stu-id="b86b6-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="b86b6-147">Nel codice seguente viene illustrata una classe che implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) utilizzando questo oggetto helper.</span><span class="sxs-lookup"><span data-stu-id="b86b6-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="b86b6-148">Questa classe definisce un metodo di **arresto** pubblico che arresta la coda degli eventi e rilascia il puntatore della coda degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b86b6-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="b86b6-149">Questo comportamento è tipico per le origini dei supporti e i sink multimediali, che hanno sempre un metodo di **arresto** .</span><span class="sxs-lookup"><span data-stu-id="b86b6-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="b86b6-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b86b6-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b86b6-151">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b86b6-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



