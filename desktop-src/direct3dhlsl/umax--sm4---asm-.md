---
title: Umax (SM4-ASM)
description: Unsigned Integer al massimo per componente.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398239"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="b5bfb-103">Umax (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b5bfb-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="b5bfb-104">Unsigned Integer al massimo per componente.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="b5bfb-105">Umax dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="b5bfb-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="b5bfb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b5bfb-106">Item</span></span>                                                            | <span data-ttu-id="b5bfb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5bfb-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bfb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b5bfb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b5bfb-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="b5bfb-110">*dest*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="b5bfb-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="b5bfb-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="b5bfb-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="b5bfb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b5bfb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b5bfb-113">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="b5bfb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b5bfb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b5bfb-115">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b5bfb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5bfb-116">Remarks</span></span>

<span data-ttu-id="b5bfb-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5bfb-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b5bfb-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="b5bfb-118">Vertex Shader</span></span> | <span data-ttu-id="b5bfb-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="b5bfb-119">Geometry Shader</span></span> | <span data-ttu-id="b5bfb-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="b5bfb-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b5bfb-121">x</span><span class="sxs-lookup"><span data-stu-id="b5bfb-121">x</span></span>             | <span data-ttu-id="b5bfb-122">x</span><span class="sxs-lookup"><span data-stu-id="b5bfb-122">x</span></span>               | <span data-ttu-id="b5bfb-123">x</span><span class="sxs-lookup"><span data-stu-id="b5bfb-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b5bfb-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b5bfb-124">Minimum Shader Model</span></span>

<span data-ttu-id="b5bfb-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b5bfb-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b5bfb-126">Shader Model</span></span>                                              | <span data-ttu-id="b5bfb-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="b5bfb-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b5bfb-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b5bfb-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b5bfb-129">sì</span><span class="sxs-lookup"><span data-stu-id="b5bfb-129">yes</span></span>       |
| [<span data-ttu-id="b5bfb-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b5bfb-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b5bfb-131">sì</span><span class="sxs-lookup"><span data-stu-id="b5bfb-131">yes</span></span>       |
| [<span data-ttu-id="b5bfb-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b5bfb-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b5bfb-133">sì</span><span class="sxs-lookup"><span data-stu-id="b5bfb-133">yes</span></span>       |
| [<span data-ttu-id="b5bfb-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5bfb-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b5bfb-135">no</span><span class="sxs-lookup"><span data-stu-id="b5bfb-135">no</span></span>        |
| [<span data-ttu-id="b5bfb-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5bfb-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b5bfb-137">no</span><span class="sxs-lookup"><span data-stu-id="b5bfb-137">no</span></span>        |
| [<span data-ttu-id="b5bfb-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5bfb-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b5bfb-139">no</span><span class="sxs-lookup"><span data-stu-id="b5bfb-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b5bfb-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5bfb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5bfb-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5bfb-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





