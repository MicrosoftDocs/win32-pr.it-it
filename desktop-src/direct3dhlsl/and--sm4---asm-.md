---
title: e (SM4-ASM)
description: AND bit per bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719444"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="12fd6-103">e (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="12fd6-103">and (sm4 - asm)</span></span>

<span data-ttu-id="12fd6-104">**And** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="12fd6-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="12fd6-105">e dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="12fd6-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="12fd6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="12fd6-106">Item</span></span>                                                            | <span data-ttu-id="12fd6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12fd6-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="12fd6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="12fd6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="12fd6-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="12fd6-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="12fd6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="12fd6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="12fd6-111">\[nel \] valore a 32 bit per **e** con *src1*.</span><span class="sxs-lookup"><span data-stu-id="12fd6-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="12fd6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="12fd6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="12fd6-113">\[nel \] valore a 32 bit per **e** con *src0*.</span><span class="sxs-lookup"><span data-stu-id="12fd6-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="12fd6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="12fd6-114">Remarks</span></span>

<span data-ttu-id="12fd6-115">Logica dei componenti **e** di ogni coppia di valori a 32 bit da *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="12fd6-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="12fd6-116">I risultati a 32 bit vengono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="12fd6-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="12fd6-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="12fd6-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="12fd6-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="12fd6-118">Vertex Shader</span></span> | <span data-ttu-id="12fd6-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="12fd6-119">Geometry Shader</span></span> | <span data-ttu-id="12fd6-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="12fd6-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="12fd6-121">x</span><span class="sxs-lookup"><span data-stu-id="12fd6-121">x</span></span>             | <span data-ttu-id="12fd6-122">x</span><span class="sxs-lookup"><span data-stu-id="12fd6-122">x</span></span>               | <span data-ttu-id="12fd6-123">x</span><span class="sxs-lookup"><span data-stu-id="12fd6-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12fd6-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="12fd6-124">Minimum Shader Model</span></span>

<span data-ttu-id="12fd6-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="12fd6-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="12fd6-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="12fd6-126">Shader Model</span></span>                                              | <span data-ttu-id="12fd6-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="12fd6-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="12fd6-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="12fd6-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="12fd6-129">sì</span><span class="sxs-lookup"><span data-stu-id="12fd6-129">yes</span></span>       |
| [<span data-ttu-id="12fd6-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="12fd6-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="12fd6-131">sì</span><span class="sxs-lookup"><span data-stu-id="12fd6-131">yes</span></span>       |
| [<span data-ttu-id="12fd6-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="12fd6-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="12fd6-133">sì</span><span class="sxs-lookup"><span data-stu-id="12fd6-133">yes</span></span>       |
| [<span data-ttu-id="12fd6-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12fd6-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="12fd6-135">no</span><span class="sxs-lookup"><span data-stu-id="12fd6-135">no</span></span>        |
| [<span data-ttu-id="12fd6-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12fd6-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="12fd6-137">no</span><span class="sxs-lookup"><span data-stu-id="12fd6-137">no</span></span>        |
| [<span data-ttu-id="12fd6-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12fd6-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="12fd6-139">no</span><span class="sxs-lookup"><span data-stu-id="12fd6-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="12fd6-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12fd6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12fd6-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12fd6-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





