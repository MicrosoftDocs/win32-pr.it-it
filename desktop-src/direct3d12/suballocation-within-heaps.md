---
title: Sottoallocazione negli heap
description: Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104158"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="ab969-103">Sottoallocazione negli heap</span><span class="sxs-lookup"><span data-stu-id="ab969-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="ab969-104">Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro).</span><span class="sxs-lookup"><span data-stu-id="ab969-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ab969-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ab969-105">In this section</span></span>



| <span data-ttu-id="ab969-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="ab969-106">Topic</span></span>                                                                                       | <span data-ttu-id="ab969-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab969-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab969-108">Alias di memoria ed ereditarietà dei dati</span><span class="sxs-lookup"><span data-stu-id="ab969-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="ab969-109">La risorsa posizionata e riservata potrebbe avere l'alias della memoria fisica in un heap.</span><span class="sxs-lookup"><span data-stu-id="ab969-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="ab969-110">Le risorse posizionate abilitano più scenari di ereditarietà dei dati rispetto alle risorse riservate quando l'heap dispone del flag condiviso impostato o quando le risorse con alias hanno layout di memoria completamente definiti.</span><span class="sxs-lookup"><span data-stu-id="ab969-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="ab969-111">Heap condivisi</span><span class="sxs-lookup"><span data-stu-id="ab969-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="ab969-112">La condivisione è utile per le architetture a più processi e a più adapter.</span><span class="sxs-lookup"><span data-stu-id="ab969-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="ab969-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab969-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab969-114">**ID3D12Device:: Createheap ha provocato**</span><span class="sxs-lookup"><span data-stu-id="ab969-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="ab969-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="ab969-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="ab969-116">Gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="ab969-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





