---
description: Flag di funzionalità pixel shader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995268"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="bedb4-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bedb4-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="bedb4-104">Flag di funzionalità pixel shader.</span><span class="sxs-lookup"><span data-stu-id="bedb4-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="bedb4-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="bedb4-105">\#define</span></span>                                     | <span data-ttu-id="bedb4-106">Valore</span><span class="sxs-lookup"><span data-stu-id="bedb4-106">Value</span></span>          | <span data-ttu-id="bedb4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bedb4-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedb4-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="bedb4-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="bedb4-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="bedb4-109">(1 << 0)</span></span> | <span data-ttu-id="bedb4-110">La swizzling arbitraria è supportata.</span><span class="sxs-lookup"><span data-stu-id="bedb4-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="bedb4-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="bedb4-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="bedb4-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="bedb4-112">(1 << 1)</span></span> | <span data-ttu-id="bedb4-113">Sono supportate le istruzioni per la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="bedb4-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="bedb4-114">PREDICATO D3DD3DPSHADERCAPS2 \_ 0 \_</span><span class="sxs-lookup"><span data-stu-id="bedb4-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="bedb4-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="bedb4-115">(1 << 2)</span></span> | <span data-ttu-id="bedb4-116">Il predicato dell'istruzione è supportato.</span><span class="sxs-lookup"><span data-stu-id="bedb4-116">Instruction predication is supported.</span></span> <span data-ttu-id="bedb4-117">Vedere [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="bedb4-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="bedb4-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="bedb4-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="bedb4-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="bedb4-119">(1 << 3)</span></span> | <span data-ttu-id="bedb4-120">Non esiste alcun limite al numero di operazioni di lettura dipendenti per ogni istruzione.</span><span class="sxs-lookup"><span data-stu-id="bedb4-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="bedb4-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="bedb4-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="bedb4-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="bedb4-122">(1 << 4)</span></span> | <span data-ttu-id="bedb4-123">Non esiste alcun limite al numero di istruzioni tex.</span><span class="sxs-lookup"><span data-stu-id="bedb4-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="bedb4-124">D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bedb4-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="bedb4-125">24</span><span class="sxs-lookup"><span data-stu-id="bedb4-125">24</span></span>             | <span data-ttu-id="bedb4-126">Livello massimo di annidamento delle istruzioni di controllo dinamico del flusso (break, breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="bedb4-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="bedb4-127">D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bedb4-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="bedb4-128">0</span><span class="sxs-lookup"><span data-stu-id="bedb4-128">0</span></span>              | <span data-ttu-id="bedb4-129">Livello minimo di annidamento delle istruzioni di controllo dinamico del flusso (break, breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="bedb4-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="bedb4-130">D3DPS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="bedb4-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="bedb4-131">32</span><span class="sxs-lookup"><span data-stu-id="bedb4-131">32</span></span>             | <span data-ttu-id="bedb4-132">Il driver supporterà al massimo questo numero di registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="bedb4-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="bedb4-133">D3DPS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="bedb4-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="bedb4-134">12</span><span class="sxs-lookup"><span data-stu-id="bedb4-134">12</span></span>             | <span data-ttu-id="bedb4-135">Il driver supporterà almeno questo numero di registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="bedb4-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="bedb4-136">D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bedb4-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="bedb4-137">4</span><span class="sxs-lookup"><span data-stu-id="bedb4-137">4</span></span>              | <span data-ttu-id="bedb4-138">Profondità massima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a / [rep,](../direct3dhlsl/rep---vs.md) rispetto a [call - vs](../direct3dhlsl/call---vs.md) / [callnz bool - rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni.</span><span class="sxs-lookup"><span data-stu-id="bedb4-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="bedb4-139">D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="bedb4-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="bedb4-140">1</span><span class="sxs-lookup"><span data-stu-id="bedb4-140">1</span></span>              | <span data-ttu-id="bedb4-141">La profondità minima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a / [rep,](../direct3dhlsl/rep---vs.md) rispetto a [call - vs](../direct3dhlsl/call---vs.md) / [callnz bool - rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni.</span><span class="sxs-lookup"><span data-stu-id="bedb4-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="bedb4-142">D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="bedb4-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="bedb4-143">512</span><span class="sxs-lookup"><span data-stu-id="bedb4-143">512</span></span>            | <span data-ttu-id="bedb4-144">Il driver supporterà al massimo queste numerose istruzioni.</span><span class="sxs-lookup"><span data-stu-id="bedb4-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="bedb4-145">D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="bedb4-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="bedb4-146">96</span><span class="sxs-lookup"><span data-stu-id="bedb4-146">96</span></span>             | <span data-ttu-id="bedb4-147">Il driver supporterà almeno questo numero di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="bedb4-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="bedb4-148">Queste costanti vengono usate dal membro D3DPSHADERCAPS2 \_ 0 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="bedb4-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="bedb4-149">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="bedb4-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="bedb4-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bedb4-150">Header</span></span>                   | <span data-ttu-id="bedb4-151">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="bedb4-151">d3d9caps.h</span></span> |
| <span data-ttu-id="bedb4-152">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="bedb4-152">Minimum operating system</span></span> | <span data-ttu-id="bedb4-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bedb4-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bedb4-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bedb4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bedb4-155">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="bedb4-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="bedb4-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="bedb4-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
