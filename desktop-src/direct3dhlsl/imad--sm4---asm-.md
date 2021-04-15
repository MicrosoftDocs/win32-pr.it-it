---
title: imad (SM4-ASM)
description: Intero con segno Multiply e Add.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992984"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="6a047-103">imad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a047-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="6a047-104">Intero con segno Multiply e Add.</span><span class="sxs-lookup"><span data-stu-id="6a047-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="6a047-105">imad dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] , \[ - \] src2 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="6a047-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6a047-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a047-106">Item</span></span>                                                            | <span data-ttu-id="6a047-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a047-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6a047-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6a047-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6a047-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a047-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="6a047-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6a047-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6a047-111">\[in \] value per moltiplicare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="6a047-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="6a047-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6a047-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6a047-113">\[in \] value per moltiplicare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="6a047-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="6a047-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="6a047-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="6a047-115">\[in \] valore da aggiungere al prodotto di *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="6a047-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a047-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a047-116">Remarks</span></span>

<span data-ttu-id="6a047-117">[IMUL](imul--sm4---asm-.md) a livello di componente degli operandi a 32 bit *src0* e *src1* (con segno), mantenendo i 32 bit (per componente) del risultato, seguiti da un [IAdd](iadd--sm4---asm-.md) di *src2*, producendo il risultato corretto a 32 bit (per componente).</span><span class="sxs-lookup"><span data-stu-id="6a047-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="6a047-118">I risultati a 32 bit vengono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="6a047-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="6a047-119">Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire un'operazione aritmetica.</span><span class="sxs-lookup"><span data-stu-id="6a047-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="6a047-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a047-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a047-121">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="6a047-121">Vertex Shader</span></span> | <span data-ttu-id="6a047-122">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="6a047-122">Geometry Shader</span></span> | <span data-ttu-id="6a047-123">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="6a047-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a047-124">x</span><span class="sxs-lookup"><span data-stu-id="6a047-124">x</span></span>             | <span data-ttu-id="6a047-125">x</span><span class="sxs-lookup"><span data-stu-id="6a047-125">x</span></span>               | <span data-ttu-id="6a047-126">x</span><span class="sxs-lookup"><span data-stu-id="6a047-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a047-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6a047-127">Minimum Shader Model</span></span>

<span data-ttu-id="6a047-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="6a047-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a047-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6a047-129">Shader Model</span></span>                                              | <span data-ttu-id="6a047-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="6a047-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a047-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6a047-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a047-132">sì</span><span class="sxs-lookup"><span data-stu-id="6a047-132">yes</span></span>       |
| [<span data-ttu-id="6a047-133">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="6a047-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a047-134">sì</span><span class="sxs-lookup"><span data-stu-id="6a047-134">yes</span></span>       |
| [<span data-ttu-id="6a047-135">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="6a047-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a047-136">sì</span><span class="sxs-lookup"><span data-stu-id="6a047-136">yes</span></span>       |
| [<span data-ttu-id="6a047-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a047-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a047-138">no</span><span class="sxs-lookup"><span data-stu-id="6a047-138">no</span></span>        |
| [<span data-ttu-id="6a047-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a047-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a047-140">no</span><span class="sxs-lookup"><span data-stu-id="6a047-140">no</span></span>        |
| [<span data-ttu-id="6a047-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a047-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a047-142">no</span><span class="sxs-lookup"><span data-stu-id="6a047-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a047-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a047-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a047-144">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a047-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





