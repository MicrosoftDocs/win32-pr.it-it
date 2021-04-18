---
description: Allocatore di memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocatore di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522202"
---
# <a name="memory-allocator"></a><span data-ttu-id="64b49-103">Allocatore di memoria</span><span class="sxs-lookup"><span data-stu-id="64b49-103">Memory Allocator</span></span>

<span data-ttu-id="64b49-104">L'oggetto allocatore di memoria alloca i buffer per gli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="64b49-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="64b49-105">I filtri possono utilizzare questo oggetto per allocare buffer di memoria condivisi. Tuttavia, un filtro con requisiti speciali può implementare anche il proprio oggetto allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="64b49-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="64b49-106">Creare questo oggetto chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="64b49-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="64b49-107">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="64b49-107">Class Identifier</span></span> | <span data-ttu-id="64b49-108">\_MEMORYALLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="64b49-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="64b49-109">Interfacce</span><span class="sxs-lookup"><span data-stu-id="64b49-109">Interfaces</span></span>       | [<span data-ttu-id="64b49-110">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="64b49-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="64b49-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64b49-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64b49-112">Oggetti DirectShow</span><span class="sxs-lookup"><span data-stu-id="64b49-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



