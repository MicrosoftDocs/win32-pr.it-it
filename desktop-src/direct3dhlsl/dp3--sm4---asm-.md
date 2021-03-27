---
title: DP3 (SM4-ASM)
description: vettore tridimensionale punto-prodotto dei componenti RGB, POS-Swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857758"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="a6199-103">DP3 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a6199-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="a6199-104">vettore tridimensionale punto-prodotto dei componenti RGB, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="a6199-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="a6199-105">DP3 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="a6199-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a6199-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a6199-106">Item</span></span>                                                            | <span data-ttu-id="a6199-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6199-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6199-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a6199-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a6199-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a6199-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="a6199-110">*dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b*</span><span class="sxs-lookup"><span data-stu-id="a6199-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="a6199-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a6199-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a6199-112">\[nei \] componenti di operazione.</span><span class="sxs-lookup"><span data-stu-id="a6199-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="a6199-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a6199-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a6199-114">\[nei \] componenti di operazione.</span><span class="sxs-lookup"><span data-stu-id="a6199-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a6199-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6199-115">Remarks</span></span>

<span data-ttu-id="a6199-116">Risultato scalare replicato in componenti nella maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="a6199-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="a6199-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6199-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a6199-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a6199-118">Vertex Shader</span></span> | <span data-ttu-id="a6199-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a6199-119">Geometry Shader</span></span> | <span data-ttu-id="a6199-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a6199-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a6199-121">x</span><span class="sxs-lookup"><span data-stu-id="a6199-121">x</span></span>             | <span data-ttu-id="a6199-122">x</span><span class="sxs-lookup"><span data-stu-id="a6199-122">x</span></span>               | <span data-ttu-id="a6199-123">x</span><span class="sxs-lookup"><span data-stu-id="a6199-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a6199-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a6199-124">Minimum Shader Model</span></span>

<span data-ttu-id="a6199-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6199-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a6199-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a6199-126">Shader Model</span></span>                                              | <span data-ttu-id="a6199-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="a6199-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a6199-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a6199-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a6199-129">sì</span><span class="sxs-lookup"><span data-stu-id="a6199-129">yes</span></span>       |
| [<span data-ttu-id="a6199-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a6199-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a6199-131">sì</span><span class="sxs-lookup"><span data-stu-id="a6199-131">yes</span></span>       |
| [<span data-ttu-id="a6199-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a6199-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a6199-133">sì</span><span class="sxs-lookup"><span data-stu-id="a6199-133">yes</span></span>       |
| [<span data-ttu-id="a6199-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a6199-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a6199-135">no</span><span class="sxs-lookup"><span data-stu-id="a6199-135">no</span></span>        |
| [<span data-ttu-id="a6199-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a6199-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a6199-137">no</span><span class="sxs-lookup"><span data-stu-id="a6199-137">no</span></span>        |
| [<span data-ttu-id="a6199-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a6199-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a6199-139">no</span><span class="sxs-lookup"><span data-stu-id="a6199-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a6199-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6199-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6199-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a6199-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





