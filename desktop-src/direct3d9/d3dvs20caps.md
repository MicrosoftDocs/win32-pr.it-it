---
description: Costanti di vertice shader caps. Queste costanti vengono usate dal membro VS20Caps di D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342946"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="14998-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="14998-104">D3DVS20CAPS</span></span>

<span data-ttu-id="14998-105">Costanti di vertice shader caps.</span><span class="sxs-lookup"><span data-stu-id="14998-105">Vertex shader caps constants.</span></span> <span data-ttu-id="14998-106">Queste costanti vengono usate dal membro VS20Caps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="14998-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="14998-107">\#Definire</span><span class="sxs-lookup"><span data-stu-id="14998-107">\#define</span></span>                              | <span data-ttu-id="14998-108">Valore</span><span class="sxs-lookup"><span data-stu-id="14998-108">Value</span></span>          | <span data-ttu-id="14998-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14998-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14998-110">PREDICAZIONE D3DVS20CAPS \_</span><span class="sxs-lookup"><span data-stu-id="14998-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="14998-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="14998-111">(1 << 0)</span></span> | <span data-ttu-id="14998-112">La predicazione dell'istruzione è supportata.</span><span class="sxs-lookup"><span data-stu-id="14998-112">Instruction predication is supported.</span></span> <span data-ttu-id="14998-113">Vedere [setp \_ comp - e](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="14998-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="14998-114">D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="14998-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="14998-115">24</span><span class="sxs-lookup"><span data-stu-id="14998-115">24</span></span>             | <span data-ttu-id="14998-116">Livello massimo di annidamento delle istruzioni di controllo dinamico del flusso ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="14998-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="14998-117">D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="14998-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="14998-118">0</span><span class="sxs-lookup"><span data-stu-id="14998-118">0</span></span>              | <span data-ttu-id="14998-119">Livello minimo di annidamento delle istruzioni di controllo dinamico del flusso ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="14998-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="14998-120">D3DVS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="14998-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="14998-121">32</span><span class="sxs-lookup"><span data-stu-id="14998-121">32</span></span>             | <span data-ttu-id="14998-122">Numero massimo di registri temporanei supportati.</span><span class="sxs-lookup"><span data-stu-id="14998-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="14998-123">D3DVS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="14998-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="14998-124">12</span><span class="sxs-lookup"><span data-stu-id="14998-124">12</span></span>             | <span data-ttu-id="14998-125">Numero minimo di registri temporanei supportati.</span><span class="sxs-lookup"><span data-stu-id="14998-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="14998-126">D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="14998-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="14998-127">4</span><span class="sxs-lookup"><span data-stu-id="14998-127">4</span></span>              | <span data-ttu-id="14998-128">Profondità massima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep / [e](../direct3dhlsl/rep---vs.md) [call,](../direct3dhlsl/call---vs.md)rispetto a / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni .</span><span class="sxs-lookup"><span data-stu-id="14998-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="14998-129">D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="14998-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="14998-130">1</span><span class="sxs-lookup"><span data-stu-id="14998-130">1</span></span>              | <span data-ttu-id="14998-131">Profondità minima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep e call, rispetto a / [](../direct3dhlsl/rep---vs.md) [](../direct3dhlsl/call---vs.md) / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni .</span><span class="sxs-lookup"><span data-stu-id="14998-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="14998-132">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="14998-132">Constant Information</span></span>



| <span data-ttu-id="14998-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="14998-133">Requirement</span></span>                         | <span data-ttu-id="14998-134">Valore</span><span class="sxs-lookup"><span data-stu-id="14998-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="14998-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14998-135">Header</span></span>                   | <span data-ttu-id="14998-136">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="14998-136">d3d9caps.h</span></span> |
| <span data-ttu-id="14998-137">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="14998-137">Minimum operating system</span></span> | <span data-ttu-id="14998-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="14998-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="14998-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14998-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14998-140">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="14998-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="14998-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="14998-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
