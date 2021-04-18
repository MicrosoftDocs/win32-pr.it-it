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
# <a name="media-event-generators"></a>Generatori di eventi multimediali

Media Foundation consente agli oggetti di inviare eventi in modo coerente. Un oggetto può usare gli eventi per segnalare il completamento di un metodo asincrono o per notificare all'applicazione una modifica nello stato dell'oggetto.

Se un oggetto invia eventi, espone l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Ogni volta che l'oggetto invia un nuovo evento, l'evento viene inserito in una coda. L'applicazione può richiedere l'evento successivo dalla coda chiamando uno dei metodi seguenti:

-   [**IMFMediaEventGenerator:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

Il metodo [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) è sincrono. Se un evento è già presente nella coda, il metodo restituisce immediatamente un risultato. Se nella coda non è presente alcun evento, il metodo ha esito negativo immediatamente oppure si blocca fino a quando l'evento successivo non viene accodato, a seconda del flag passato a **GetEvent**.

Il metodo [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) è asincrono, pertanto non viene mai bloccato. Questo metodo accetta un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , che deve essere implementata dall'applicazione. Quando viene richiamato il callback, l'applicazione chiama [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ottenere l'evento dalla coda. Per altre informazioni su **IMFAsyncCallback**, vedere [metodi di callback asincroni](asynchronous-callback-methods.md).

Gli eventi sono rappresentati dall'interfaccia [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) . Questa interfaccia presenta i metodi seguenti:

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Recupera il tipo di evento. Il tipo di evento indica che cosa è successo ad attivare l'evento.

-   [**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Recupera un valore **HRESULT** che indica se l'operazione che ha attivato l'evento è stata eseguita correttamente. Se un'operazione ha esito negativo in modo asincrono, **GetStatus** restituisce un codice di errore.

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Recupera un **PROPVARIANT** che contiene i dati dell'evento. I dati dell'evento dipendono dal tipo di evento. Alcuni eventi non contengono dati.

-   [**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Recupera un **GUID**. Questo metodo si applica all' [evento MEExtendedType](meextendedtype.md)e fornisce un modo per definire eventi personalizzati.

L'interfaccia [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) eredita anche l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Alcuni eventi contengono informazioni aggiuntive come attributi.

Per un elenco dei tipi di evento e i relativi dati e attributi associati, vedere [eventi Media Foundation](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implementazione di IMFMediaEventGenerator

Se si sta scrivendo un componente plug-in per Media Foundation, ad esempio un'origine multimediale personalizzata o un sink multimediale, potrebbe essere necessario implementare [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator). Per semplificare questa operazione, Media Foundation fornisce un oggetto helper che implementa una coda degli eventi. Creare la coda degli eventi chiamando la funzione [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) . La coda degli eventi espone l'interfaccia [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) . Nell'implementazione dell'oggetto dei metodi **IMFMediaEventGenerator** , chiamare il metodo corrispondente nella coda degli eventi.

L'oggetto coda di eventi è thread-safe. Non mantenere mai lo stesso oggetto sezione critica quando si chiamano [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) e [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), perché **GetEvent** potrebbe bloccarsi per un tempo indefinito in attesa di [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent). Se si tiene la stessa sezione critica per entrambi i metodi, verrà generato un deadlock.

Prima di rilasciare la coda degli eventi, chiamare [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) per rilasciare le risorse detenute dall'oggetto.

Quando l'oggetto deve generare un evento, chiamare uno dei metodi seguenti nella coda degli eventi:

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Questi metodi inseriscono un nuovo evento nella coda e segnalano qualsiasi chiamante in attesa dell'evento successivo.

Nel codice seguente viene illustrata una classe che implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) utilizzando questo oggetto helper. Questa classe definisce un metodo di **arresto** pubblico che arresta la coda degli eventi e rilascia il puntatore della coda degli eventi. Questo comportamento è tipico per le origini dei supporti e i sink multimediali, che hanno sempre un metodo di **arresto** .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



