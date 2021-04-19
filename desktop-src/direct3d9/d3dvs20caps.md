---
description: Costanti caps del vertex shader. Queste costanti vengono usate dal membro VS20Caps di D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304992"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="13147-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="13147-104">D3DVS20CAPS</span></span>

<span data-ttu-id="13147-105">Costanti caps del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="13147-105">Vertex shader caps constants.</span></span> <span data-ttu-id="13147-106">Queste costanti vengono usate dal membro VS20Caps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="13147-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="13147-107">\#definire</span><span class="sxs-lookup"><span data-stu-id="13147-107">\#define</span></span>                              | <span data-ttu-id="13147-108">Valore</span><span class="sxs-lookup"><span data-stu-id="13147-108">Value</span></span>          | <span data-ttu-id="13147-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13147-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13147-110">\_Predicazione D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="13147-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="13147-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="13147-111">(1 << 0)</span></span> | <span data-ttu-id="13147-112">L'istruzione predicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="13147-112">Instruction predication is supported.</span></span> <span data-ttu-id="13147-113">Vedere [setp \_ comp-vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="13147-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="13147-114">D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="13147-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="13147-115">24</span><span class="sxs-lookup"><span data-stu-id="13147-115">24</span></span>             | <span data-ttu-id="13147-116">Il livello massimo di nidificazione delle istruzioni per il controllo dinamico del flusso ([Break-vs](../direct3dhlsl/break---vs.md), [break \_ comp-vs](../direct3dhlsl/break-comp---vs.md), [Breakp-](../direct3dhlsl/breakp---vs.md)vs, [if \_ comp-vs](../direct3dhlsl/if-comp---vs.md), if comp \_ -vs, se [predazione](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="13147-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="13147-117">D3DVS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="13147-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="13147-118">0</span><span class="sxs-lookup"><span data-stu-id="13147-118">0</span></span>              | <span data-ttu-id="13147-119">Il livello minimo di nidificazione delle istruzioni per il controllo dinamico del flusso ([Break-vs](../direct3dhlsl/break---vs.md), [break \_ comp-vs](../direct3dhlsl/break-comp---vs.md), [Breakp-](../direct3dhlsl/breakp---vs.md)vs, [if \_ comp-vs](../direct3dhlsl/if-comp---vs.md), if comp \_ -vs, se [predazione](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="13147-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="13147-120">D3DVS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="13147-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="13147-121">32</span><span class="sxs-lookup"><span data-stu-id="13147-121">32</span></span>             | <span data-ttu-id="13147-122">Numero massimo di registri temporanei supportati.</span><span class="sxs-lookup"><span data-stu-id="13147-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="13147-123">D3DVS20 \_ Min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="13147-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="13147-124">12</span><span class="sxs-lookup"><span data-stu-id="13147-124">12</span></span>             | <span data-ttu-id="13147-125">Numero minimo di registri temporanei supportati.</span><span class="sxs-lookup"><span data-stu-id="13147-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="13147-126">D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="13147-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="13147-127">4</span><span class="sxs-lookup"><span data-stu-id="13147-127">4</span></span>              | <span data-ttu-id="13147-128">Profondità massima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="13147-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="13147-129">D3DVS20 \_ Min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="13147-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="13147-130">1</span><span class="sxs-lookup"><span data-stu-id="13147-130">1</span></span>              | <span data-ttu-id="13147-131">Profondità minima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="13147-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="13147-132">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="13147-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="13147-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13147-133">Header</span></span>                   | <span data-ttu-id="13147-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="13147-134">d3d9caps.h</span></span> |
| <span data-ttu-id="13147-135">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="13147-135">Minimum operating system</span></span> | <span data-ttu-id="13147-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="13147-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="13147-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13147-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13147-138">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="13147-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="13147-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="13147-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
