---
description: Flag di funzionalità pixel shader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127534"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="378c8-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="378c8-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="378c8-104">Flag di funzionalità pixel shader.</span><span class="sxs-lookup"><span data-stu-id="378c8-104">Pixel shader capability flags.</span></span>



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378c8-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="378c8-105">\#define</span></span>                                     | <span data-ttu-id="378c8-106">Valore</span><span class="sxs-lookup"><span data-stu-id="378c8-106">Value</span></span>          | <span data-ttu-id="378c8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="378c8-107">Description</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="378c8-108">\_ARBITRARYSWIZZLE D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="378c8-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="378c8-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="378c8-109">(1 << 0)</span></span> | <span data-ttu-id="378c8-110">Il swizzling arbitrario è supportato.</span><span class="sxs-lookup"><span data-stu-id="378c8-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="378c8-111">\_GRADIENTINSTRUCTIONS D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="378c8-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="378c8-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="378c8-112">(1 << 1)</span></span> | <span data-ttu-id="378c8-113">Sono supportate le istruzioni per la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="378c8-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="378c8-114">\_Predicazione D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="378c8-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="378c8-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="378c8-115">(1 << 2)</span></span> | <span data-ttu-id="378c8-116">L'istruzione predicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="378c8-116">Instruction predication is supported.</span></span> <span data-ttu-id="378c8-117">Vedere [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="378c8-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="378c8-118">\_NODEPENDENTREADLIMIT D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="378c8-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="378c8-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="378c8-119">(1 << 3)</span></span> | <span data-ttu-id="378c8-120">Non esiste alcun limite al numero di letture dipendenti per istruzione.</span><span class="sxs-lookup"><span data-stu-id="378c8-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="378c8-121">\_NOTEXINSTRUCTIONLIMIT D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="378c8-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="378c8-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="378c8-122">(1 << 4)</span></span> | <span data-ttu-id="378c8-123">Non esiste alcun limite al numero di istruzioni Tex.</span><span class="sxs-lookup"><span data-stu-id="378c8-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="378c8-124">D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="378c8-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="378c8-125">24</span><span class="sxs-lookup"><span data-stu-id="378c8-125">24</span></span>             | <span data-ttu-id="378c8-126">Il livello massimo di nidificazione delle istruzioni di controllo del flusso dinamico (Break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="378c8-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="378c8-127">D3DPS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="378c8-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="378c8-128">0</span><span class="sxs-lookup"><span data-stu-id="378c8-128">0</span></span>              | <span data-ttu-id="378c8-129">Il livello minimo di nidificazione delle istruzioni di controllo del flusso dinamico (Break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="378c8-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="378c8-130">D3DPS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="378c8-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="378c8-131">32</span><span class="sxs-lookup"><span data-stu-id="378c8-131">32</span></span>             | <span data-ttu-id="378c8-132">Il driver supporterà al massimo questo numero di registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="378c8-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="378c8-133">D3DPS20 \_ Min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="378c8-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="378c8-134">12</span><span class="sxs-lookup"><span data-stu-id="378c8-134">12</span></span>             | <span data-ttu-id="378c8-135">Il driver supporterà almeno questo numero di registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="378c8-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="378c8-136">D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="378c8-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="378c8-137">4</span><span class="sxs-lookup"><span data-stu-id="378c8-137">4</span></span>              | <span data-ttu-id="378c8-138">Profondità massima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="378c8-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="378c8-139">D3DPS20 \_ Min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="378c8-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="378c8-140">1</span><span class="sxs-lookup"><span data-stu-id="378c8-140">1</span></span>              | <span data-ttu-id="378c8-141">Profondità minima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="378c8-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="378c8-142">D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="378c8-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="378c8-143">512</span><span class="sxs-lookup"><span data-stu-id="378c8-143">512</span></span>            | <span data-ttu-id="378c8-144">Il driver supporterà al massimo questo numero di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="378c8-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="378c8-145">D3DPS20 \_ Min \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="378c8-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="378c8-146">96</span><span class="sxs-lookup"><span data-stu-id="378c8-146">96</span></span>             | <span data-ttu-id="378c8-147">Il driver supporterà almeno questo numero di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="378c8-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="378c8-148">Queste costanti vengono usate dal \_ membro D3DPSHADERCAPS2 0 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="378c8-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="378c8-149">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="378c8-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="378c8-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="378c8-150">Header</span></span>                   | <span data-ttu-id="378c8-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="378c8-151">d3d9caps.h</span></span> |
| <span data-ttu-id="378c8-152">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="378c8-152">Minimum operating system</span></span> | <span data-ttu-id="378c8-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="378c8-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="378c8-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="378c8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="378c8-155">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="378c8-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="378c8-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="378c8-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
