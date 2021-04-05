---
Description: Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Confronto tra i metodi di allocazione della memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969287"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="b4779-103">Confronto tra i metodi di allocazione della memoria</span><span class="sxs-lookup"><span data-stu-id="b4779-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="b4779-104">Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria:</span><span class="sxs-lookup"><span data-stu-id="b4779-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="b4779-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="b4779-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="b4779-107">**HeapAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="b4779-108">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="b4779-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-109">**malloc**</span></span>
-   <span data-ttu-id="b4779-110">**Nuovo**</span><span class="sxs-lookup"><span data-stu-id="b4779-110">**new**</span></span>
-   [<span data-ttu-id="b4779-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4779-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="b4779-112">Sebbene le funzioni [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) riallocano la memoria dallo stesso heap, ognuna fornisce un set di funzionalità leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="b4779-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="b4779-113">Ad esempio, è possibile indicare a **HeapAlloc** di generare un'eccezione se non è stato possibile allocare memoria, una funzionalità non disponibile con **LocalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4779-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="b4779-114">**LocalAlloc** supporta l'allocazione di handle che consentono lo spostamento della memoria sottostante da parte di una riallocazione senza modificare il valore dell'handle, una funzionalità non disponibile con **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4779-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="b4779-115">A partire da Windows a 32 bit, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) vengono implementati come funzioni wrapper che chiamano [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando un handle per l'heap predefinito del processo.</span><span class="sxs-lookup"><span data-stu-id="b4779-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="b4779-116">Pertanto, **GlobalAlloc** e **LocalAlloc** hanno un overhead maggiore di **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="b4779-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="b4779-117">Poiché i diversi allocatori di heap forniscono funzionalità distintive usando meccanismi diversi, è necessario liberare memoria con la funzione corretta.</span><span class="sxs-lookup"><span data-stu-id="b4779-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="b4779-118">Ad esempio, la memoria allocata con [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve essere liberata con [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e non con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) o [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span><span class="sxs-lookup"><span data-stu-id="b4779-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="b4779-119">La memoria allocata con [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve essere sottoposta a query, convalidata e rilasciata con la funzione globale o locale corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b4779-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="b4779-120">La funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) consente di specificare opzioni aggiuntive per l'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="b4779-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="b4779-121">Tuttavia, le relative allocazioni utilizzano una granularità di pagina, pertanto l'utilizzo di **VirtualAlloc** può comportare un utilizzo maggiore della memoria.</span><span class="sxs-lookup"><span data-stu-id="b4779-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="b4779-122">La funzione **malloc** presenta lo svantaggio di essere dipendente dalla fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b4779-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="b4779-123">L'operatore **New** presenta lo svantaggio di essere dipendente dal compilatore e dipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="b4779-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="b4779-124">La funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) offre il vantaggio di funzionare correttamente in C, C++ o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b4779-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="b4779-125">È anche l'unico modo per condividere memoria in un'applicazione basata su COM, perché MIDL USA **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per effettuare il marshalling della memoria.</span><span class="sxs-lookup"><span data-stu-id="b4779-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="b4779-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="b4779-126">Examples</span></span>

* [<span data-ttu-id="b4779-127">Riserva e commit della memoria</span><span class="sxs-lookup"><span data-stu-id="b4779-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="b4779-128">Esempio AWE</span><span class="sxs-lookup"><span data-stu-id="b4779-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="b4779-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4779-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4779-130">Funzioni globali e locali</span><span class="sxs-lookup"><span data-stu-id="b4779-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="b4779-131">Funzioni heap</span><span class="sxs-lookup"><span data-stu-id="b4779-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="b4779-132">Funzioni di memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="b4779-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 