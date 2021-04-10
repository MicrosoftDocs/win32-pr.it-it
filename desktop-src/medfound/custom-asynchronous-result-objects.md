---
description: Oggetti risultato asincrono personalizzati
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Oggetti risultato asincrono personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5a0109b47255bc14fcccafbbb09c419848b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225823"
---
# <a name="custom-asynchronous-result-objects"></a>Oggetti risultato asincrono personalizzati

In questo argomento viene descritto come implementare l'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .

È raro che sia necessario scrivere un'implementazione personalizzata dell'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . In quasi tutti i casi, l'implementazione di Media Foundation standard è sufficiente. Questa implementazione viene restituita dalla funzione [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) . Tuttavia, se si scrive un'implementazione personalizzata, è necessario tenere presenti alcuni aspetti.

In primo luogo, l'implementazione deve ereditare la struttura [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) . Le code di lavoro Media Foundation utilizzano questa struttura internamente per inviare l'operazione. Inizializzare tutti i membri della struttura su zero, ad eccezione del membro **pCallback** , che contiene un puntatore all'interfaccia di callback del chiamante.

In secondo luogo, l'oggetto deve chiamare [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) nel costruttore per bloccare la piattaforma Media Foundation. Chiamare [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) per sbloccare la piattaforma. Queste funzioni consentono di impedire l'arresto della piattaforma prima che l'oggetto venga eliminato definitivamente. Per altre informazioni, vedere [code di lavoro](work-queues.md).

Nel codice seguente viene illustrata un'implementazione di base dell'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Come illustrato, questo codice non fornisce funzionalità aggiuntive oltre all'implementazione di Media Foundation standard.


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Code di lavoro](work-queues.md)
</dt> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> </dl>

 

 



