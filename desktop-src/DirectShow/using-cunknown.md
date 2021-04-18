---
description: DirectShow implementa IUnknown in una classe di base denominata CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Uso di CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314399"
---
# <a name="using-cunknown"></a><span data-ttu-id="31934-103">Uso di CUnknown</span><span class="sxs-lookup"><span data-stu-id="31934-103">Using CUnknown</span></span>

<span data-ttu-id="31934-104">DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in una classe di base denominata [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="31934-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="31934-105">È possibile utilizzare **CUnknown** per derivare altre classi, eseguendo l'override solo dei metodi che cambiano tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="31934-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="31934-106">La maggior parte delle altre classi di base in DirectShow derivano da **CUnknown**, quindi il componente può ereditare direttamente da **CUnknown** o da un'altra classe di base.</span><span class="sxs-lookup"><span data-stu-id="31934-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="31934-107">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="31934-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="31934-108">[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="31934-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="31934-109">Gestisce i conteggi dei riferimenti internamente e nella maggior parte dei casi la classe derivata può ereditare i due metodi di conteggio dei riferimenti senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="31934-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="31934-110">Tenere presente che **CUnknown** si elimina quando il conteggio dei riferimenti scende a zero.</span><span class="sxs-lookup"><span data-stu-id="31934-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="31934-111">D'altra parte, è necessario eseguire l'override di [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), perché il metodo nella classe di base restituisce E \_ nointerface se riceve un IID diverso da IID \_ IUnknown.</span><span class="sxs-lookup"><span data-stu-id="31934-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="31934-112">Nella classe derivata testare il IID di interfacce supportate, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="31934-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="31934-113">La funzione di utilità [**GetInterface**](getinterface.md) (vedere [**funzioni helper com**](com-helper-functions.md)) imposta il puntatore, incrementa il conteggio dei riferimenti in modo thread-safe e restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31934-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="31934-114">Nel caso predefinito, chiamare il metodo della classe base e restituire il risultato.</span><span class="sxs-lookup"><span data-stu-id="31934-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="31934-115">Se si deriva da un'altra classe di base, chiamare invece il relativo metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="31934-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="31934-116">In questo modo è possibile supportare tutte le interfacce supportate dalla classe padre.</span><span class="sxs-lookup"><span data-stu-id="31934-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="31934-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="31934-117">IUnknown</span></span>

<span data-ttu-id="31934-118">Come indicato in precedenza, la versione delegante di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è la stessa per ogni componente, poiché non esegue alcuna operazione oltre a richiamare l'istanza corretta della versione non delegata.</span><span class="sxs-lookup"><span data-stu-id="31934-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="31934-119">Per praticità, il file di intestazione ComBase. h contiene una macro, [**Declare \_ IUnknown**](declare-iunknown.md), che dichiara i tre metodi delegati come metodi inline.</span><span class="sxs-lookup"><span data-stu-id="31934-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="31934-120">Espande il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="31934-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="31934-121">La funzione di utilità [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera un puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente proprietario di questo componente.</span><span class="sxs-lookup"><span data-stu-id="31934-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="31934-122">Per un componente aggregato, il proprietario è il componente esterno.</span><span class="sxs-lookup"><span data-stu-id="31934-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="31934-123">In caso contrario, il componente è proprietario.</span><span class="sxs-lookup"><span data-stu-id="31934-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="31934-124">Includere la \_ macro DECLARE IUnknown nella sezione public della definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="31934-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="31934-125">Costruttore di classe</span><span class="sxs-lookup"><span data-stu-id="31934-125">Class Constructor</span></span>

<span data-ttu-id="31934-126">Il costruttore della classe deve richiamare il metodo del costruttore per la classe padre, oltre a qualsiasi elemento che è specifico della classe.</span><span class="sxs-lookup"><span data-stu-id="31934-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="31934-127">Nell'esempio seguente viene riportato un tipico metodo del costruttore:</span><span class="sxs-lookup"><span data-stu-id="31934-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="31934-128">Il metodo accetta i parametri seguenti, che passano direttamente al metodo del costruttore [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="31934-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="31934-129">*tszName* specifica un nome per il componente.</span><span class="sxs-lookup"><span data-stu-id="31934-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="31934-130">il *punk* è un puntatore all' [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="31934-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="31934-131">*pHr* è un puntatore a un valore HRESULT che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="31934-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="31934-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="31934-132">Summary</span></span>

<span data-ttu-id="31934-133">Nell'esempio seguente viene illustrata una classe derivata che supporta [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un'interfaccia ipotetica denominata ISomeInterface:</span><span class="sxs-lookup"><span data-stu-id="31934-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="31934-134">Questo esempio illustra i punti seguenti:</span><span class="sxs-lookup"><span data-stu-id="31934-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="31934-135">La classe [**CUnknown**](cunknown.md) implementa l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="31934-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="31934-136">Il nuovo componente eredita da **CUnknown** e da tutte le interfacce supportate dal componente.</span><span class="sxs-lookup"><span data-stu-id="31934-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="31934-137">Il componente può derivare invece da un'altra classe di base che eredita da **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="31934-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="31934-138">La macro [**Declare \_ IUnknown**](declare-iunknown.md) dichiara i metodi [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) deleganti come metodi inline.</span><span class="sxs-lookup"><span data-stu-id="31934-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="31934-139">La classe [**CUnknown**](cunknown.md) fornisce l'implementazione di per [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="31934-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="31934-140">Per supportare un'interfaccia diversa da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la classe derivata deve eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) e verificare l'IID della nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="31934-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="31934-141">Il costruttore della classe richiama il metodo del costruttore per [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="31934-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="31934-142">Il passaggio successivo per la scrittura di un filtro consiste nel consentire a un'applicazione di creare nuove istanze del componente.</span><span class="sxs-lookup"><span data-stu-id="31934-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="31934-143">Questa operazione richiede una conoscenza delle dll e della relativa relazione con le class factory e i metodi del costruttore di classe.</span><span class="sxs-lookup"><span data-stu-id="31934-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="31934-144">Per ulteriori informazioni, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="31934-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31934-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31934-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31934-146">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="31934-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
