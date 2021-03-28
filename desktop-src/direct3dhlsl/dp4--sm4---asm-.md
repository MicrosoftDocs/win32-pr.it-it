---
title: DP4 (SM4-ASM)
description: vettore 4 dimensionale-prodotto dei componenti RGBA, POS-Swizzle.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a91a253d4e8b53bc044e658c3fe75d8f7547da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956073"
---
# <a name="dp4-sm4---asm"></a><span data-ttu-id="44841-103">DP4 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="44841-103">dp4 (sm4 - asm)</span></span>

<span data-ttu-id="44841-104">vettore 4 dimensionale-prodotto dei componenti RGBA, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="44841-104">4-dimensional vector dot-product of components rgba, POS-swizzle.</span></span>



| <span data-ttu-id="44841-105">DP4 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="44841-105">dp4\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="44841-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="44841-106">Item</span></span>                                                            | <span data-ttu-id="44841-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44841-107">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44841-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="44841-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="44841-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="44841-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="44841-110">*dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* src1. \* *b* +  *src0. a* \* *src1. a*</span><span class="sxs-lookup"><span data-stu-id="44841-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*+ *src0.a* \* *src1.a*</span></span><br/> |
| <span data-ttu-id="44841-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="44841-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="44841-112">\[nei \] componenti di operazione.</span><span class="sxs-lookup"><span data-stu-id="44841-112">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |
| <span data-ttu-id="44841-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="44841-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="44841-114">\[nei \] componenti di operazione.</span><span class="sxs-lookup"><span data-stu-id="44841-114">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="44841-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="44841-115">Remarks</span></span>

<span data-ttu-id="44841-116">Risultato scalare replicato in componenti nella maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="44841-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="44841-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="44841-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="44841-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="44841-118">Vertex Shader</span></span> | <span data-ttu-id="44841-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="44841-119">Geometry Shader</span></span> | <span data-ttu-id="44841-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="44841-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="44841-121">x</span><span class="sxs-lookup"><span data-stu-id="44841-121">x</span></span>             | <span data-ttu-id="44841-122">x</span><span class="sxs-lookup"><span data-stu-id="44841-122">x</span></span>               | <span data-ttu-id="44841-123">x</span><span class="sxs-lookup"><span data-stu-id="44841-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="44841-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="44841-124">Minimum Shader Model</span></span>

<span data-ttu-id="44841-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="44841-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44841-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="44841-126">Shader Model</span></span>                                              | <span data-ttu-id="44841-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="44841-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="44841-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="44841-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="44841-129">sì</span><span class="sxs-lookup"><span data-stu-id="44841-129">yes</span></span>       |
| [<span data-ttu-id="44841-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="44841-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="44841-131">sì</span><span class="sxs-lookup"><span data-stu-id="44841-131">yes</span></span>       |
| [<span data-ttu-id="44841-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="44841-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="44841-133">sì</span><span class="sxs-lookup"><span data-stu-id="44841-133">yes</span></span>       |
| [<span data-ttu-id="44841-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44841-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="44841-135">no</span><span class="sxs-lookup"><span data-stu-id="44841-135">no</span></span>        |
| [<span data-ttu-id="44841-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44841-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="44841-137">no</span><span class="sxs-lookup"><span data-stu-id="44841-137">no</span></span>        |
| [<span data-ttu-id="44841-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44841-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="44841-139">no</span><span class="sxs-lookup"><span data-stu-id="44841-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="44841-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44841-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44841-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44841-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





