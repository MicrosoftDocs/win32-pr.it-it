---
title: Allocazione di memoria in COM
description: Allocazione di memoria in COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103889"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="7fffd-103">Allocazione di memoria in COM</span><span class="sxs-lookup"><span data-stu-id="7fffd-103">Memory Allocation in COM</span></span>

<span data-ttu-id="7fffd-104">In alcuni casi un metodo alloca un buffer di memoria nell'heap e restituisce l'indirizzo del buffer al chiamante.</span><span class="sxs-lookup"><span data-stu-id="7fffd-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="7fffd-105">COM definisce una coppia di funzioni per allocare e liberare memoria nell'heap.</span><span class="sxs-lookup"><span data-stu-id="7fffd-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="7fffd-106">La [**funzione CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alloca un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="7fffd-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="7fffd-107">La [**funzione CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un blocco di memoria allocato con [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="7fffd-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="7fffd-108">È stato illustrato un esempio di questo modello nella [finestra di dialogo Apri :](example--the-open-dialog-box.md)</span><span class="sxs-lookup"><span data-stu-id="7fffd-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="7fffd-109">Il [**metodo GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) alloca memoria per una stringa.</span><span class="sxs-lookup"><span data-stu-id="7fffd-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="7fffd-110">Internamente, il metodo chiama [**CoTaskMemAlloc per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) allocare la stringa.</span><span class="sxs-lookup"><span data-stu-id="7fffd-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="7fffd-111">Quando il metodo viene restituito, *pszFilePath* punta alla posizione di memoria del nuovo buffer.</span><span class="sxs-lookup"><span data-stu-id="7fffd-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="7fffd-112">Il chiamante è responsabile della chiamata [**a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="7fffd-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="7fffd-113">Perché COM definisce le proprie funzioni di allocazione della memoria?</span><span class="sxs-lookup"><span data-stu-id="7fffd-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="7fffd-114">Uno dei motivi consiste nel fornire un livello di astrazione sull'allocatore dell'heap.</span><span class="sxs-lookup"><span data-stu-id="7fffd-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="7fffd-115">In caso contrario, alcuni metodi potrebbero chiamare **malloc** mentre altri chiamano **new**.</span><span class="sxs-lookup"><span data-stu-id="7fffd-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="7fffd-116">Il programma dovrà quindi chiamare gratuitamente **in** alcuni casi ed eliminare **in** altri e tenere traccia di tutto sarebbe diventato rapidamente impossibile.</span><span class="sxs-lookup"><span data-stu-id="7fffd-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="7fffd-117">Le funzioni di allocazione COM creano un approccio uniforme.</span><span class="sxs-lookup"><span data-stu-id="7fffd-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="7fffd-118">Un'altra considerazione è il fatto che COM è *uno* standard binario, quindi non è associato a un linguaggio di programmazione specifico.</span><span class="sxs-lookup"><span data-stu-id="7fffd-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="7fffd-119">Com non può pertanto basarsi su alcuna forma di allocazione di memoria specifica del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="7fffd-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="7fffd-120">Prossima</span><span class="sxs-lookup"><span data-stu-id="7fffd-120">Next</span></span>

[<span data-ttu-id="7fffd-121">Procedure di codifica COM</span><span class="sxs-lookup"><span data-stu-id="7fffd-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
