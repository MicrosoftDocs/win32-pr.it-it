---
description: Generatori di eventi multimediali
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Generatori di eventi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24bd37b347fb06f97448b43241a1da40123195b63b9191b97581be60d7378ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724161"
---
# <a name="media-event-generators"></a>Generatori di eventi multimediali

Media Foundation un modo coerente per gli oggetti di inviare eventi. Un oggetto può usare eventi per segnalare il completamento di un metodo asincrono o per notificare all'applicazione una modifica nello stato dell'oggetto.

Se un oggetto invia eventi, espone [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Ogni volta che l'oggetto invia un nuovo evento, l'evento viene inserito in una coda. L'applicazione può richiedere l'evento successivo dalla coda chiamando uno dei metodi seguenti:

-   [**IMFMediaEventGenerator::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

Il [**metodo GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) è sincrono. Se un evento è già presente nella coda, il metodo restituisce immediatamente un risultato. Se non è presente alcun evento nella coda, il metodo ha esito negativo immediatamente o si blocca fino a quando l'evento successivo non viene accodato, a seconda del flag passato a **GetEvent.**

Il [**metodo BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) è asincrono, quindi non si blocca mai. Questo metodo accetta un puntatore [**all'interfaccia IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) che l'applicazione deve implementare. Quando viene richiamato il callback, l'applicazione chiama [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ottenere l'evento dalla coda. Per altre informazioni su **IMFAsyncCallback,** vedere [Metodi di callback asincroni.](asynchronous-callback-methods.md)

Gli eventi sono rappresentati [**dall'interfaccia IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) Questa interfaccia dispone dei metodi seguenti:

-   [**GetType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)recupera il tipo di evento. Il tipo di evento indica cosa è successo per attivare l'evento.

-   [**GetStatus:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)recupera un valore **HRESULT** che indica se l'operazione che ha attivato l'evento è riuscita. Se un'operazione non riesce in modo asincrono, **GetStatus** restituisce un codice di errore.

-   [**GetValue:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)recupera un oggetto **PROPVARIANT** che contiene i dati dell'evento. I dati dell'evento dipendono dal tipo di evento. Alcuni eventi non hanno dati.

-   [**GetExtendedType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)recupera un **GUID**. Questo metodo si applica [all'evento MEExtendedType](meextendedtype.md)e consente di definire eventi personalizzati.

[**L'interfaccia IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) eredita anche [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Alcuni eventi trasportano informazioni aggiuntive come attributi.

Per un elenco dei tipi di evento e dei relativi dati e attributi associati, [vedere Media Foundation eventi](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implementazione di IMFMediaEventGenerator

Se si scrive un componente plug-in per Media Foundation, ad esempio un'origine multimediale personalizzata o un sink multimediale, potrebbe essere necessario implementare [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Per semplificare questa operazione, Media Foundation un oggetto helper che implementa una coda di eventi. Creare la coda eventi chiamando la [**funzione MFCreateEventQueue.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) La coda eventi espone [**l'interfaccia IMFMediaEventQueue.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) Nell'implementazione dell'oggetto dei **metodi IMFMediaEventGenerator** chiamare il metodo corrispondente nella coda degli eventi.

L'oggetto coda eventi è thread-safe. Non mantenere mai lo stesso oggetto sezione critica quando si chiamano [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) e [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), perché **GetEvent** potrebbe bloccarsi per un periodo illimitato in attesa di [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent). Se si contiene la stessa sezione critica per entrambi i metodi, si verifica un deadlock.

Prima di rilasciare la coda di eventi, chiamare [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) per rilasciare le risorse che l'oggetto contiene.

Quando l'oggetto deve generare un evento, chiamare uno dei metodi seguenti nella coda degli eventi:

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Questi metodi consentono di inserire un nuovo evento nella coda e di segnalare qualsiasi chiamante in attesa dell'evento successivo.

Il codice seguente illustra una classe che implementa [**IMFMediaEventGenerator usando**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) questo oggetto helper. Questa classe definisce un metodo **Shutdown** pubblico che arresta la coda degli eventi e rilascia il puntatore della coda di eventi. Questo comportamento è tipico per le origini multimediali e i sink multimediali, che hanno sempre un **metodo Shutdown.**


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

[API Media Foundation platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 



