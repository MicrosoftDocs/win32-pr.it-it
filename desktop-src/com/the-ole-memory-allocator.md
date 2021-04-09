---
title: Allocatore di memoria OLE
description: Allocatore di memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118507"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="4c3ca-103">Allocatore di memoria OLE</span><span class="sxs-lookup"><span data-stu-id="4c3ca-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="4c3ca-104">La libreria COM fornisce un'implementazione di un allocatore di memoria thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4c3ca-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="4c3ca-105">Ovvero non può causare problemi nelle situazioni multithread. Ogni volta che la proprietà di un blocco allocato di memoria viene passata attraverso un'interfaccia COM o tra un client e la libreria COM, è necessario usare questo allocatore COM per allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="4c3ca-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="4c3ca-106">L'allocazione interna a un oggetto può utilizzare qualsiasi schema di allocazione desiderato, ma l'allocatore di memoria COM è un allocatore pratico, efficiente e thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4c3ca-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="4c3ca-107">Una chiamata alla funzione API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fornisce un puntatore all'allocatore OLE, che è un'implementazione dell'interfaccia [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="4c3ca-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="4c3ca-108">Tuttavia, è più efficiente chiamare le funzioni di supporto [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)e [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), che eseguono il wrapping di un puntatore all'allocatore di memoria delle attività, chiamando il metodo **IMalloc** corrispondente e quindi rilasciando il puntatore all'allocatore.</span><span class="sxs-lookup"><span data-stu-id="4c3ca-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c3ca-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c3ca-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c3ca-110">Gestione dell'allocazione di memoria</span><span class="sxs-lookup"><span data-stu-id="4c3ca-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="4c3ca-111">Libreria COM</span><span class="sxs-lookup"><span data-stu-id="4c3ca-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 