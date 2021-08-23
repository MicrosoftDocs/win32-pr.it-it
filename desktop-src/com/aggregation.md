---
title: Aggregazione
description: L'aggregazione è il meccanismo di riutilizzo degli oggetti in cui l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate nell'oggetto esterno stesso.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4855b1fa3a614d190b8f192aeee2e7cf3d3d53bbdce589a1363e0398f70430c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731721"
---
# <a name="aggregation"></a>Aggregazione

L'aggregazione è il meccanismo di riutilizzo degli oggetti in cui l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate nell'oggetto esterno stesso. Ciò è utile quando l'oggetto esterno delega ogni chiamata a una delle relative interfacce alla stessa interfaccia nell'oggetto interno. In questo caso, l'aggregazione è disponibile per evitare un sovraccarico aggiuntivo di implementazione nell'oggetto esterno. L'aggregazione è in realtà un caso specializzato [di contenimento/delega.](containment-delegation.md)

L'aggregazione è quasi semplice da implementare come il contenimento, ad eccezione delle tre [**funzioni IUnknown:**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Il catch è che dal punto di vista del client, qualsiasi **funzione IUnknown** nell'oggetto esterno deve influire sull'oggetto esterno. In altri, **AddRef** e **Release** influiscono sull'oggetto esterno e **QueryInterface** espone tutte le interfacce disponibili nell'oggetto esterno. Tuttavia, se l'oggetto esterno espone semplicemente l'interfaccia di un oggetto interno come propria, i membri **IUnknown** dell'oggetto interno chiamati tramite tale interfaccia si comporteranno in modo diverso rispetto ai membri **IUnknown** nelle interfacce dell'oggetto esterno, una violazione assoluta delle regole e delle proprietà che governano **IUnknown**.

La soluzione è che l'aggregazione richiede un'implementazione esplicita di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) nell'oggetto interno e la delega dei **metodi IUnknown** di qualsiasi altra interfaccia ai metodi **IUnknown dell'oggetto esterno.**

## <a name="creating-aggregable-objects"></a>Creazione di oggetti aggregabili

La creazione di oggetti che possono essere aggregati è facoltativa. Tuttavia, è semplice da eseguire e offre vantaggi significativi. Le regole seguenti si applicano alla creazione di un oggetto aggregabile:

-   L'implementazione aggregabile (o interna) dell'oggetto [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controlla il conteggio dei riferimenti dell'oggetto interno e questa implementazione non deve delegare all'oggetto esterno sconosciuto (il controllo **IUnknown**).
-   L'implementazione aggregabile (o interna) dell'oggetto [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per le altre interfacce deve delegare all'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo e non deve influire direttamente sul conteggio dei riferimenti dell'oggetto interno.
-   [**L'interfaccia IUnknown interna**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) deve [**implementare QueryInterface solo**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'oggetto interno.
-   L'oggetto aggregabile non deve chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) quando contiene un riferimento al puntatore [**IUnknown di**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controllo.
-   Quando viene creato l'oggetto, se viene richiesta un'interfaccia diversa da [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) la creazione deve avere esito negativo con E \_ NOINTERFACE.

Il frammento di codice seguente illustra un'implementazione corretta di un oggetto aggregabile usando il metodo della classe annidata di implementazione delle interfacce:


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a>Aggregazione di oggetti

Quando si sviluppa un oggetto aggregabile, si applicano le regole seguenti:

-   Quando si crea l'oggetto interno, l'oggetto esterno deve richiedere in modo esplicito il relativo [**oggetto IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
-   L'oggetto esterno deve proteggere l'implementazione di [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dalla reentrancy con un conteggio dei riferimenti artificiale intorno al codice di distruzione.
-   L'oggetto esterno deve chiamare il metodo di controllo **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) se esegue una query per un puntatore a una delle interfacce dell'oggetto interno. Per liberare questo puntatore, l'oggetto esterno chiama il relativo metodo [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) **IUnknown** di controllo, seguito da **Release** sul puntatore dell'oggetto interno.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   L'oggetto esterno non deve delegare una query per qualsiasi interfaccia non riconosciuta all'oggetto interno, a meno che tale comportamento non sia specificamente l'intenzione dell'oggetto esterno.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenimento/delega](containment-delegation.md)
</dt> </dl>

 

 