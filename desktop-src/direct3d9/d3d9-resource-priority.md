---
description: Costanti utilizzate per impostare la priorità di una risorsa in priorità.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234969"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="aaad6-103">\_Priorità delle risorse d3d9 \_</span><span class="sxs-lookup"><span data-stu-id="aaad6-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="aaad6-104">Costanti utilizzate per impostare la priorità di una risorsa in [**priorità**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span><span class="sxs-lookup"><span data-stu-id="aaad6-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="aaad6-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="aaad6-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="aaad6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaad6-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="aaad6-107"><dt>**D3d9 \_ 0x28000000 \_ priorità \_ minima risorsa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="aaad6-108">La risorsa ha la priorità più bassa possibile.</span><span class="sxs-lookup"><span data-stu-id="aaad6-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="aaad6-109">Questa costante contrassegna la risorsa come inutilizzata e per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="aaad6-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="aaad6-110">La risorsa deve essere rimossa non appena un'altra risorsa richiede lo spazio di memoria occupato dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="aaad6-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="aaad6-111"><dt>**D3d9 \_ \_Priorità \_ bassa della risorsa**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="aaad6-112">La risorsa è pianificata con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="aaad6-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="aaad6-113">Il posizionamento della risorsa non è critico e il sistema operativo esegue un lavoro minimo per trovare una posizione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aaad6-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="aaad6-114">Contrassegnare una risorsa come priorità bassa consente ad altre risorse più importanti di occupare la memoria più veloce.</span><span class="sxs-lookup"><span data-stu-id="aaad6-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="aaad6-115"><dt>**D3d9 \_ 0x78000000 \_ \_ normale priorità risorsa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="aaad6-116">La risorsa è pianificata con priorità normale.</span><span class="sxs-lookup"><span data-stu-id="aaad6-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="aaad6-117">La posizione della risorsa è importante per le prestazioni, ma non è fondamentale.</span><span class="sxs-lookup"><span data-stu-id="aaad6-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="aaad6-118">Il sistema operativo deve provare a collocare la risorsa contrassegnata come normale nella posizione preferita della risorsa invece che in una risorsa con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="aaad6-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="aaad6-119">In genere, le trame sono contrassegnate come normali.</span><span class="sxs-lookup"><span data-stu-id="aaad6-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="aaad6-120"><dt>**D3d9 \_ Priorità di risorsa \_ \_ elevata**</dt> <dt>0xA0000000</dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="aaad6-121">La risorsa è pianificata con priorità alta.</span><span class="sxs-lookup"><span data-stu-id="aaad6-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="aaad6-122">La posizione della risorsa è essenziale per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="aaad6-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="aaad6-123">Il sistema operativo tenta sempre di collocare la risorsa contrassegnata come elevata nella posizione preferita della risorsa invece che con una risorsa con priorità bassa o con priorità normale.</span><span class="sxs-lookup"><span data-stu-id="aaad6-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="aaad6-124">In genere, le destinazioni di rendering sono contrassegnate come High.</span><span class="sxs-lookup"><span data-stu-id="aaad6-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="aaad6-125"><dt>**D3d9 \_ 0xc8000000 \_ priorità \_ massima risorsa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="aaad6-126">La risorsa ha la massima priorità possibile.</span><span class="sxs-lookup"><span data-stu-id="aaad6-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="aaad6-127">Questa costante contrassegna la priorità della risorsa come aggiunta temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="aaad6-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="aaad6-128">Una risorsa aggiunta temporaneamente viene rimossa dalla memoria solo se non è possibile risolvere il requisito di memoria di un buffer DMA.</span><span class="sxs-lookup"><span data-stu-id="aaad6-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="aaad6-129">Il sistema operativo tenta di suddividere un buffer DMA fino alla dimensione minima e di rimuovere tutte le altre risorse che non sono bloccate e non aggiunte temporaneamente prima di rimuovere una risorsa aggiunta temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="aaad6-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="aaad6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaad6-130">Remarks</span></span>

<span data-ttu-id="aaad6-131">Valori diversi dalla **\_ priorità della risorsa d3d9 \_ \_ Minimum** e la **\_ \_ priorità \_ massima della risorsa d3d9** vengono considerati come hint dall'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="aaad6-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="aaad6-132">È possibile utilizzare livelli di priorità diversi dai valori definiti in precedenza in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="aaad6-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="aaad6-133">Ad esempio, contrassegnare una risorsa con un livello di priorità di 0x78000001 indica che la priorità delle risorse è leggermente superiore al normale.</span><span class="sxs-lookup"><span data-stu-id="aaad6-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaad6-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaad6-134">Requirements</span></span>



| <span data-ttu-id="aaad6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaad6-135">Requirement</span></span> | <span data-ttu-id="aaad6-136">Valore</span><span class="sxs-lookup"><span data-stu-id="aaad6-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaad6-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aaad6-137">Header</span></span><br/> | <dl> <span data-ttu-id="aaad6-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaad6-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaad6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaad6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaad6-140">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="aaad6-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
