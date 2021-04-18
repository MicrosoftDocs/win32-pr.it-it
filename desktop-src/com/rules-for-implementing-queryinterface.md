---
title: Regole per l'implementazione di QueryInterface
description: Regole per l'implementazione di QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300501"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="e2a5c-103">Regole per l'implementazione di QueryInterface</span><span class="sxs-lookup"><span data-stu-id="e2a5c-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="e2a5c-104">Esistono tre regole principali che regolano l'implementazione del metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) su un oggetto com:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="e2a5c-105">Gli oggetti devono avere Identity.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-105">Objects must have identity.</span></span>
-   <span data-ttu-id="e2a5c-106">Il set di interfacce in un'istanza di oggetto deve essere statico.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="e2a5c-107">Deve essere possibile eseguire una query corretta per qualsiasi interfaccia di un oggetto da qualsiasi altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="e2a5c-108">Gli oggetti devono avere identità</span><span class="sxs-lookup"><span data-stu-id="e2a5c-108">Objects Must Have Identity</span></span>

<span data-ttu-id="e2a5c-109">Per ogni istanza di oggetto specificata, una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IUnknown deve sempre restituire lo stesso valore del puntatore fisico.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="e2a5c-110">In questo modo è possibile chiamare **QueryInterface** su due interfacce e confrontare i risultati per determinare se puntano alla stessa istanza di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="e2a5c-111">Il set di interfacce in un'istanza di oggetto deve essere statico</span><span class="sxs-lookup"><span data-stu-id="e2a5c-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="e2a5c-112">Il set di interfacce accessibili in un oggetto tramite [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) deve essere statico e non dinamico.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="e2a5c-113">In particolare, se **QueryInterface** restituisce \_ un valore OK per un determinato IID una volta, non deve mai restituire E \_ nointerface sulle chiamate successive sullo stesso oggetto. Se **QueryInterface** restituisce e \_ nointerface per un determinato IID, le chiamate successive per lo stesso IID sullo stesso oggetto non devono mai restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="e2a5c-114">Deve essere possibile eseguire query correttamente per qualsiasi interfaccia di un oggetto da qualsiasi altra interfaccia</span><span class="sxs-lookup"><span data-stu-id="e2a5c-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="e2a5c-115">Ovvero, dato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="e2a5c-116">si applicano le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-116">the following rules apply:</span></span>

-   <span data-ttu-id="e2a5c-117">Se si dispone di un puntatore a un'interfaccia su un oggetto, una chiamata come la seguente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per la stessa interfaccia deve avere esito positivo:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="e2a5c-118">Se una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per un secondo puntatore di interfaccia ha esito positivo, anche una chiamata a **QueryInterface** da tale puntatore per la prima interfaccia deve avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="e2a5c-119">Se pB è stato ottenuto correttamente, è necessario che venga eseguita anche la seguente operazione:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="e2a5c-120">Qualsiasi interfaccia deve essere in grado di eseguire query per qualsiasi altra interfaccia in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="e2a5c-121">Se pB è stato ottenuto correttamente ed è stata eseguita una query per una terza interfaccia (IC) usando tale puntatore, è necessario anche essere in grado di eseguire query correttamente per IC usando il primo puntatore, pA.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="e2a5c-122">In questo caso, la sequenza seguente deve avere esito positivo:</span><span class="sxs-lookup"><span data-stu-id="e2a5c-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="e2a5c-123">Le implementazioni dell'interfaccia devono mantenere un contatore dei riferimenti di puntatore in attesa a tutte le interfacce su un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="e2a5c-124">Usare un **unsigned integer** per il contatore.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="e2a5c-125">Se un client deve tenere presente che le risorse sono state liberate, deve usare un metodo in un'interfaccia nell'oggetto con una semantica di livello superiore prima di chiamare [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="e2a5c-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2a5c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2a5c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a5c-127">Uso e implementazione di IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2a5c-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 