---
title: Aggregazione
description: L'aggregazione è il meccanismo di riutilizzo degli oggetti in cui l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate sull'oggetto esterno stesso.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339342"
---
# <a name="aggregation"></a><span data-ttu-id="9c745-103">Aggregazione</span><span class="sxs-lookup"><span data-stu-id="9c745-103">Aggregation</span></span>

<span data-ttu-id="9c745-104">L'aggregazione è il meccanismo di riutilizzo degli oggetti in cui l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate sull'oggetto esterno stesso.</span><span class="sxs-lookup"><span data-stu-id="9c745-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="9c745-105">Questa operazione è utile quando l'oggetto esterno delega ogni chiamata a una delle relative interfacce alla stessa interfaccia nell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="9c745-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="9c745-106">L'aggregazione è disponibile per praticità, in questo caso, per evitare un sovraccarico di implementazione aggiuntivo nell'oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="9c745-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="9c745-107">L'aggregazione è in realtà un caso specializzato di [contenimento/delega](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="9c745-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="9c745-108">L'aggregazione è quasi semplice da implementare come contenimento, ad eccezione delle tre funzioni [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="9c745-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="9c745-109">Il catch è che dal punto di vista del client, qualsiasi funzione **IUnknown** nell'oggetto esterno deve influire sull'oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="9c745-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="9c745-110">Ovvero **AddRef** e **Release** influiscono sull'oggetto esterno e **QueryInterface** espone tutte le interfacce disponibili nell'oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="9c745-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="9c745-111">Tuttavia, se l'oggetto esterno espone semplicemente l'interfaccia di un oggetto interno come se fosse, i membri **IUnknown** dell'oggetto interno chiamati tramite tale interfaccia si comporteranno in modo diverso rispetto ai membri **IUnknown** sulle interfacce dell'oggetto esterno, una violazione assoluta delle regole e delle proprietà che governano **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9c745-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="9c745-112">La soluzione consiste nel caso in cui l'aggregazione richieda un'implementazione esplicita di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) nell'oggetto interno e la delega dei metodi **IUnknown** di qualsiasi altra interfaccia ai metodi **IUnknown** dell'oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="9c745-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="9c745-113">Creazione di oggetti Aggregable</span><span class="sxs-lookup"><span data-stu-id="9c745-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="9c745-114">La creazione di oggetti che possono essere aggregati è facoltativa. Tuttavia, è semplice e offre vantaggi significativi.</span><span class="sxs-lookup"><span data-stu-id="9c745-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="9c745-115">Per la creazione di un oggetto aggregable, si applicano le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c745-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="9c745-116">L'implementazione dell'oggetto aggregable (o inner) di [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per la relativa interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controlla il conteggio dei riferimenti dell'oggetto interno e questa implementazione non deve delegare all'oggetto esterno sconosciuto (l' **IUnknown** di controllo).</span><span class="sxs-lookup"><span data-stu-id="9c745-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="9c745-117">L'implementazione dell'oggetto aggregable (o inner) di [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per le altre interfacce deve delegare all' [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo e non deve influire direttamente sul conteggio dei riferimenti dell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="9c745-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="9c745-118">Il [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interno deve implementare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) solo per l'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="9c745-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="9c745-119">L'oggetto aggregable non deve chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) quando contiene un riferimento al puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo.</span><span class="sxs-lookup"><span data-stu-id="9c745-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="9c745-120">Quando viene creato l'oggetto, se è richiesta un'interfaccia diversa da [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , la creazione deve avere esito negativo con E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="9c745-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="9c745-121">Il frammento di codice seguente illustra un'implementazione corretta di un oggetto aggregable usando il metodo della classe annidata per l'implementazione di interfacce:</span><span class="sxs-lookup"><span data-stu-id="9c745-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


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



## <a name="aggregating-objects"></a><span data-ttu-id="9c745-122">Aggregazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="9c745-122">Aggregating Objects</span></span>

<span data-ttu-id="9c745-123">Quando si sviluppa un oggetto aggregable, si applicano le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c745-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="9c745-124">Quando si crea l'oggetto interno, l'oggetto esterno deve richiedere in modo esplicito il relativo [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="9c745-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="9c745-125">L'oggetto esterno deve proteggere l'implementazione del [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dalla rientranza con un conteggio dei riferimenti artificiali intorno al relativo codice di distruzione.</span><span class="sxs-lookup"><span data-stu-id="9c745-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="9c745-126">L'oggetto esterno deve chiamare il metodo di  [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) **IUnknown** di controllo se esegue una query per un puntatore a una delle interfacce dell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="9c745-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="9c745-127">Per liberare questo puntatore, l'oggetto esterno chiama il metodo **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) di controllo, seguito dalla **versione** sul puntatore dell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="9c745-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="9c745-128">L'oggetto esterno non deve delegare in modo cieco una query per un'interfaccia non riconosciuta all'oggetto interno, a meno che tale comportamento non sia specificamente intenzionale dell'oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="9c745-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c745-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c745-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c745-130">Contenimento/delega</span><span class="sxs-lookup"><span data-stu-id="9c745-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 