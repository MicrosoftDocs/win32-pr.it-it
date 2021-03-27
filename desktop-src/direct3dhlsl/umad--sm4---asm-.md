---
title: Martina (SM4-ASM)
description: Integer senza segno, moltiplicazione e aggiunta.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719393"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="3da9d-103">Martina (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3da9d-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="3da9d-104">Integer senza segno, moltiplicazione e aggiunta.</span><span class="sxs-lookup"><span data-stu-id="3da9d-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="3da9d-105">Martina dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3da9d-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="3da9d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3da9d-106">Item</span></span>                                                            | <span data-ttu-id="3da9d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3da9d-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3da9d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3da9d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3da9d-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3da9d-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="3da9d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3da9d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3da9d-111">\[nel \] valore da moltiplicare per *src1*.</span><span class="sxs-lookup"><span data-stu-id="3da9d-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="3da9d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3da9d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3da9d-113">\[nel \] valore da moltiplicare per *src1*.</span><span class="sxs-lookup"><span data-stu-id="3da9d-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="3da9d-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="3da9d-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="3da9d-115">\[nel \] valore da aggiungere al prodotto di *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="3da9d-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3da9d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3da9d-116">Remarks</span></span>

<span data-ttu-id="3da9d-117">[Umul](umul--sm4---asm-.md) di elementi a 32 bit *src0* e *src1* senza segno, mantenendo i 32 bit bassi, per componente, del risultato.</span><span class="sxs-lookup"><span data-stu-id="3da9d-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="3da9d-118">Questa istruzione esegue quindi un [IAdd](iadd--sm4---asm-.md) di *src2*, producendo il risultato corretto a 32 bit (per componente).</span><span class="sxs-lookup"><span data-stu-id="3da9d-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="3da9d-119">I risultati a 32 bit vengono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="3da9d-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="3da9d-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3da9d-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3da9d-121">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="3da9d-121">Vertex Shader</span></span> | <span data-ttu-id="3da9d-122">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="3da9d-122">Geometry Shader</span></span> | <span data-ttu-id="3da9d-123">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="3da9d-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3da9d-124">x</span><span class="sxs-lookup"><span data-stu-id="3da9d-124">x</span></span>             | <span data-ttu-id="3da9d-125">x</span><span class="sxs-lookup"><span data-stu-id="3da9d-125">x</span></span>               | <span data-ttu-id="3da9d-126">x</span><span class="sxs-lookup"><span data-stu-id="3da9d-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3da9d-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3da9d-127">Minimum Shader Model</span></span>

<span data-ttu-id="3da9d-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3da9d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3da9d-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3da9d-129">Shader Model</span></span>                                              | <span data-ttu-id="3da9d-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="3da9d-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3da9d-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3da9d-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3da9d-132">sì</span><span class="sxs-lookup"><span data-stu-id="3da9d-132">yes</span></span>       |
| [<span data-ttu-id="3da9d-133">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3da9d-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3da9d-134">sì</span><span class="sxs-lookup"><span data-stu-id="3da9d-134">yes</span></span>       |
| [<span data-ttu-id="3da9d-135">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3da9d-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3da9d-136">sì</span><span class="sxs-lookup"><span data-stu-id="3da9d-136">yes</span></span>       |
| [<span data-ttu-id="3da9d-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3da9d-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3da9d-138">no</span><span class="sxs-lookup"><span data-stu-id="3da9d-138">no</span></span>        |
| [<span data-ttu-id="3da9d-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3da9d-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3da9d-140">no</span><span class="sxs-lookup"><span data-stu-id="3da9d-140">no</span></span>        |
| [<span data-ttu-id="3da9d-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3da9d-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3da9d-142">no</span><span class="sxs-lookup"><span data-stu-id="3da9d-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3da9d-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3da9d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3da9d-144">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3da9d-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





