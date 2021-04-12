---
description: Fornire un allocatore personalizzato
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Fornire un allocatore personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401159"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="59f05-103">Fornire un allocatore personalizzato</span><span class="sxs-lookup"><span data-stu-id="59f05-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="59f05-104">In questa sezione viene descritto come fornire un allocatore personalizzato per un filtro.</span><span class="sxs-lookup"><span data-stu-id="59f05-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="59f05-105">Sono descritte solo le connessioni [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , ma i passaggi per una connessione [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sono simili.</span><span class="sxs-lookup"><span data-stu-id="59f05-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="59f05-106">Definire innanzitutto una classe C++ per l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="59f05-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="59f05-107">L'allocatore può derivare da una delle classi di allocatore standard, [**CBaseAllocator**](cbaseallocator.md) o [**CMemAllocator**](cmemallocator.md), oppure è possibile creare una classe allocator completamente nuova.</span><span class="sxs-lookup"><span data-stu-id="59f05-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="59f05-108">Se si crea una nuova classe, deve esporre l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="59f05-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="59f05-109">I passaggi rimanenti variano a seconda che l'allocatore appartenga a un pin di input o a un pin di output sul filtro.</span><span class="sxs-lookup"><span data-stu-id="59f05-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="59f05-110">I pin di input svolgono un ruolo diverso rispetto ai pin di output durante la fase di negoziazione dell'allocatore, perché il pin di output seleziona infine l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="59f05-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="59f05-111">**Fornire un allocatore personalizzato per un pin di input**</span><span class="sxs-lookup"><span data-stu-id="59f05-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="59f05-112">Per fornire un allocatore per un pin di input, eseguire l'override del metodo [**CBaseInputPin:: Getallocator**](cbaseinputpin-getallocator.md) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="59f05-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="59f05-113">All'interno di questo metodo, controllare la variabile membro **\_ pAllocator m** .</span><span class="sxs-lookup"><span data-stu-id="59f05-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="59f05-114">Se questa variabile è non **null**, significa che l'allocatore è già stato selezionato per questa connessione, quindi il metodo **getallocator** deve restituire un puntatore a tale allocatore.</span><span class="sxs-lookup"><span data-stu-id="59f05-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="59f05-115">Se **m \_ PAllocator** è **null**, significa che l'allocatore non è stato selezionato, quindi il metodo **getallocator** deve restituire un puntatore all'allocatore preferito del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="59f05-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="59f05-116">In tal caso, creare un'istanza dell'allocatore personalizzato e restituire il relativo puntatore [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="59f05-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="59f05-117">Il codice seguente illustra come implementare il metodo **Getallocator** :</span><span class="sxs-lookup"><span data-stu-id="59f05-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="59f05-118">Quando il filtro upstream seleziona un allocatore, chiama il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="59f05-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="59f05-119">Eseguire l'override del metodo [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) per verificare le proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="59f05-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="59f05-120">In alcuni casi, il pin di input potrebbe rifiutare l'allocatore se non è l'allocatore personalizzato, sebbene ciò possa causare un errore dell'intera connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="59f05-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="59f05-121">**Fornire un allocatore personalizzato per un pin di output**</span><span class="sxs-lookup"><span data-stu-id="59f05-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="59f05-122">Per fornire un allocatore per un pin di output, eseguire l'override del metodo [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) per creare un'istanza dell'allocatore:</span><span class="sxs-lookup"><span data-stu-id="59f05-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="59f05-123">Per impostazione predefinita, la classe [**CBaseOutputPin**](cbaseoutputpin.md) richiede innanzitutto un allocatore dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="59f05-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="59f05-124">Se l'allocatore non è adatto, il pin di output crea il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="59f05-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="59f05-125">Per forzare la connessione a usare l'allocatore personalizzato, eseguire l'override del metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="59f05-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="59f05-126">Tuttavia, tenere presente che questo può impedire la connessione del PIN di output con determinati filtri, perché l'altro filtro potrebbe richiedere anche un allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="59f05-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="59f05-127">Una terza opzione consiste nel modificare l'ordine: provare prima l'allocatore personalizzato e quindi eseguire il fallback all'allocatore dell'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="59f05-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59f05-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59f05-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59f05-129">Negozi di allocatori</span><span class="sxs-lookup"><span data-stu-id="59f05-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 



