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
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="a62ab-103">Supporto di più callback</span><span class="sxs-lookup"><span data-stu-id="a62ab-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="a62ab-104">Se si chiama più di un metodo asincrono, ognuno di essi richiede un'implementazione separata di [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="a62ab-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="a62ab-105">Tuttavia, potrebbe essere necessario implementare i callback all'interno di una singola classe C++.</span><span class="sxs-lookup"><span data-stu-id="a62ab-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="a62ab-106">La classe può avere un solo metodo **Invoke** , quindi una soluzione consiste nel fornire una classe helper **che delega le** chiamate a un altro metodo in una classe contenitore.</span><span class="sxs-lookup"><span data-stu-id="a62ab-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="a62ab-107">Il codice seguente illustra un modello di classe denominato `AsyncCallback` , che illustra questo approccio.</span><span class="sxs-lookup"><span data-stu-id="a62ab-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


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



<span data-ttu-id="a62ab-108">Il parametro del modello è il nome della classe contenitore.</span><span class="sxs-lookup"><span data-stu-id="a62ab-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="a62ab-109">Il `AsyncCallback` costruttore dispone di due parametri: un puntatore alla classe del contenitore e l'indirizzo di un metodo di callback nella classe del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a62ab-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="a62ab-110">La classe contenitore può includere più istanze della `AsyncCallback` classe come variabili membro, una per ogni metodo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a62ab-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="a62ab-111">Quando la classe contenitore chiama un metodo asincrono, usa l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell' `AsyncCallback` oggetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="a62ab-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="a62ab-112">Quando `AsyncCallback` viene chiamato il metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto, la chiamata viene delegata al metodo corretto sulla classe del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a62ab-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="a62ab-113">L' `AsyncCallback` oggetto delega anche le chiamate **AddRef** e **Release** alla classe contenitore, quindi la classe contenitore gestisce la durata dell' `AsyncCallback` oggetto.</span><span class="sxs-lookup"><span data-stu-id="a62ab-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="a62ab-114">Ciò garantisce che l' `AsyncCallback` oggetto non verrà eliminato fino a quando non viene eliminato l'oggetto contenitore stesso.</span><span class="sxs-lookup"><span data-stu-id="a62ab-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="a62ab-115">Il codice seguente illustra come usare questo modello:</span><span class="sxs-lookup"><span data-stu-id="a62ab-115">The following code shows how to use this template:</span></span>


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



<span data-ttu-id="a62ab-116">In questo esempio, la classe contenitore è denominata `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="a62ab-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="a62ab-117">La variabile membro *\_ CB m* è un `AsyncCallback` oggetto.</span><span class="sxs-lookup"><span data-stu-id="a62ab-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="a62ab-118">Nel `CMyObject` costruttore la variabile membro *\_ CB m* viene inizializzata con l'indirizzo del `CMyObject::OnInvoke` metodo.</span><span class="sxs-lookup"><span data-stu-id="a62ab-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a62ab-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a62ab-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a62ab-120">Metodi di callback asincroni</span><span class="sxs-lookup"><span data-stu-id="a62ab-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



