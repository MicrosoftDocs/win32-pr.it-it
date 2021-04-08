---
description: Supporto di più callback
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Supporto di più callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755263"
---
# <a name="supporting-multiple-callbacks"></a>Supporto di più callback

Se si chiama più di un metodo asincrono, ognuno di essi richiede un'implementazione separata di [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Tuttavia, potrebbe essere necessario implementare i callback all'interno di una singola classe C++. La classe può avere un solo metodo **Invoke** , quindi una soluzione consiste nel fornire una classe helper **che delega le** chiamate a un altro metodo in una classe contenitore.

Il codice seguente illustra un modello di classe denominato `AsyncCallback` , che illustra questo approccio.


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



Il parametro del modello è il nome della classe contenitore. Il `AsyncCallback` costruttore dispone di due parametri: un puntatore alla classe del contenitore e l'indirizzo di un metodo di callback nella classe del contenitore. La classe contenitore può includere più istanze della `AsyncCallback` classe come variabili membro, una per ogni metodo asincrono. Quando la classe contenitore chiama un metodo asincrono, usa l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell' `AsyncCallback` oggetto appropriato. Quando `AsyncCallback` viene chiamato il metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto, la chiamata viene delegata al metodo corretto sulla classe del contenitore.

L' `AsyncCallback` oggetto delega anche le chiamate **AddRef** e **Release** alla classe contenitore, quindi la classe contenitore gestisce la durata dell' `AsyncCallback` oggetto. Ciò garantisce che l' `AsyncCallback` oggetto non verrà eliminato fino a quando non viene eliminato l'oggetto contenitore stesso.

Il codice seguente illustra come usare questo modello:


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



In questo esempio, la classe contenitore è denominata `CMyObject` . La variabile membro *\_ CB m* è un `AsyncCallback` oggetto. Nel `CMyObject` costruttore la variabile membro *\_ CB m* viene inizializzata con l'indirizzo del `CMyObject::OnInvoke` metodo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> </dl>

 

 



