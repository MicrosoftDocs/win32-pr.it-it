---
description: Allocatore di memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocatore di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909420"
---
# <a name="memory-allocator"></a><span data-ttu-id="2d44e-103">Allocatore di memoria</span><span class="sxs-lookup"><span data-stu-id="2d44e-103">Memory Allocator</span></span>

<span data-ttu-id="2d44e-104">L'oggetto allocatore di memoria alloca buffer per campioni di supporti.</span><span class="sxs-lookup"><span data-stu-id="2d44e-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="2d44e-105">I filtri possono usare questo oggetto per allocare buffer di memoria condivisa. Tuttavia, un filtro con requisiti speciali può anche implementare il proprio oggetto allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="2d44e-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="2d44e-106">Creare questo oggetto chiamando **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="2d44e-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="2d44e-107">Label</span><span class="sxs-lookup"><span data-stu-id="2d44e-107">Label</span></span> | <span data-ttu-id="2d44e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2d44e-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="2d44e-109">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="2d44e-109">Class Identifier</span></span> | <span data-ttu-id="2d44e-110">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="2d44e-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="2d44e-111">Interfacce</span><span class="sxs-lookup"><span data-stu-id="2d44e-111">Interfaces</span></span>       | [<span data-ttu-id="2d44e-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="2d44e-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="2d44e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d44e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d44e-114">DirectShow Objects</span><span class="sxs-lookup"><span data-stu-id="2d44e-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



