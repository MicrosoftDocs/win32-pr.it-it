---
title: IMUL (SM4-ASM)
description: Intero con segno Multiply.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719423"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="19470-103">IMUL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="19470-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="19470-104">Intero con segno Multiply.</span><span class="sxs-lookup"><span data-stu-id="19470-104">Signed integer multiply.</span></span>



| <span data-ttu-id="19470-105">IMUL destHI \[ . mask \] , destLO \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="19470-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="19470-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="19470-106">Item</span></span>                                                                                           | <span data-ttu-id="19470-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19470-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="19470-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="19470-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="19470-109">\[nell' \] indirizzo dei bit 32 alti del risultato.</span><span class="sxs-lookup"><span data-stu-id="19470-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="19470-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="19470-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="19470-111">\[nell' \] indirizzo dei bit 32 bassi del risultato.</span><span class="sxs-lookup"><span data-stu-id="19470-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="19470-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="19470-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="19470-113">\[nel \] valore da moltiplicare per *src1*.</span><span class="sxs-lookup"><span data-stu-id="19470-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="19470-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="19470-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="19470-115">\[nel \] valore da moltiplicare per *src0*.</span><span class="sxs-lookup"><span data-stu-id="19470-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="19470-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="19470-116">Remarks</span></span>

<span data-ttu-id="19470-117">Moltiplicazione componente per gli operandi a 32 bit *src0* e *src1* (entrambi firmati), producendo il risultato corretto a 64 bit completo (per componente).</span><span class="sxs-lookup"><span data-stu-id="19470-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="19470-118">I 32 bit bassi (per componente) sono posizionati in *destLO*.</span><span class="sxs-lookup"><span data-stu-id="19470-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="19470-119">I 32 bit alti (per componente) sono posizionati in *destHI*.</span><span class="sxs-lookup"><span data-stu-id="19470-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="19470-120">È possibile specificare *destHI* o *destLO* come null anziché specificare un registro, se non sono necessari i bit 32 massimi o bassi del risultato 64 bit.</span><span class="sxs-lookup"><span data-stu-id="19470-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="19470-121">Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire un'operazione aritmetica.</span><span class="sxs-lookup"><span data-stu-id="19470-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="19470-122">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="19470-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="19470-123">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="19470-123">Vertex Shader</span></span> | <span data-ttu-id="19470-124">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="19470-124">Geometry Shader</span></span> | <span data-ttu-id="19470-125">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="19470-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="19470-126">x</span><span class="sxs-lookup"><span data-stu-id="19470-126">x</span></span>             | <span data-ttu-id="19470-127">x</span><span class="sxs-lookup"><span data-stu-id="19470-127">x</span></span>               | <span data-ttu-id="19470-128">x</span><span class="sxs-lookup"><span data-stu-id="19470-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="19470-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="19470-129">Minimum Shader Model</span></span>

<span data-ttu-id="19470-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="19470-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="19470-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="19470-131">Shader Model</span></span>                                              | <span data-ttu-id="19470-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="19470-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="19470-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="19470-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="19470-134">sì</span><span class="sxs-lookup"><span data-stu-id="19470-134">yes</span></span>       |
| [<span data-ttu-id="19470-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="19470-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="19470-136">sì</span><span class="sxs-lookup"><span data-stu-id="19470-136">yes</span></span>       |
| [<span data-ttu-id="19470-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="19470-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="19470-138">sì</span><span class="sxs-lookup"><span data-stu-id="19470-138">yes</span></span>       |
| [<span data-ttu-id="19470-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19470-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="19470-140">no</span><span class="sxs-lookup"><span data-stu-id="19470-140">no</span></span>        |
| [<span data-ttu-id="19470-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19470-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="19470-142">no</span><span class="sxs-lookup"><span data-stu-id="19470-142">no</span></span>        |
| [<span data-ttu-id="19470-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19470-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="19470-144">no</span><span class="sxs-lookup"><span data-stu-id="19470-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="19470-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19470-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19470-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19470-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





