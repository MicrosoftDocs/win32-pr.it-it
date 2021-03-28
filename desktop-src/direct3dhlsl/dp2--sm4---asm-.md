---
title: DP2 (SM4-ASM)
description: 2-dimensional Vector dot-prodotto dei componenti RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398215"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="38b66-103">DP2 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="38b66-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="38b66-104">2-dimensional Vector dot-prodotto dei componenti RG, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="38b66-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="38b66-105">DP2 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="38b66-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="38b66-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="38b66-106">Item</span></span>                                                            | <span data-ttu-id="38b66-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38b66-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b66-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="38b66-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="38b66-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="38b66-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="38b66-110">*dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*</span><span class="sxs-lookup"><span data-stu-id="38b66-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="38b66-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="38b66-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="38b66-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="38b66-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="38b66-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="38b66-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="38b66-114">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="38b66-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="38b66-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="38b66-115">Remarks</span></span>

<span data-ttu-id="38b66-116">Risultato scalare replicato in componenti nella maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="38b66-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="38b66-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="38b66-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="38b66-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="38b66-118">Vertex Shader</span></span> | <span data-ttu-id="38b66-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="38b66-119">Geometry Shader</span></span> | <span data-ttu-id="38b66-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="38b66-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="38b66-121">x</span><span class="sxs-lookup"><span data-stu-id="38b66-121">x</span></span>             | <span data-ttu-id="38b66-122">x</span><span class="sxs-lookup"><span data-stu-id="38b66-122">x</span></span>               | <span data-ttu-id="38b66-123">x</span><span class="sxs-lookup"><span data-stu-id="38b66-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="38b66-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="38b66-124">Minimum Shader Model</span></span>

<span data-ttu-id="38b66-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="38b66-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="38b66-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="38b66-126">Shader Model</span></span>                                              | <span data-ttu-id="38b66-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="38b66-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="38b66-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="38b66-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="38b66-129">sì</span><span class="sxs-lookup"><span data-stu-id="38b66-129">yes</span></span>       |
| [<span data-ttu-id="38b66-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="38b66-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="38b66-131">sì</span><span class="sxs-lookup"><span data-stu-id="38b66-131">yes</span></span>       |
| [<span data-ttu-id="38b66-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="38b66-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="38b66-133">sì</span><span class="sxs-lookup"><span data-stu-id="38b66-133">yes</span></span>       |
| [<span data-ttu-id="38b66-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b66-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="38b66-135">no</span><span class="sxs-lookup"><span data-stu-id="38b66-135">no</span></span>        |
| [<span data-ttu-id="38b66-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b66-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="38b66-137">no</span><span class="sxs-lookup"><span data-stu-id="38b66-137">no</span></span>        |
| [<span data-ttu-id="38b66-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b66-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="38b66-139">no</span><span class="sxs-lookup"><span data-stu-id="38b66-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="38b66-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38b66-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b66-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b66-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





