---
title: Umin (SM4-ASM)
description: Unsigned Integer minimo per i componenti.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 059b9660e4969b252c867a009a920259c92bff18
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117193"
---
# <a name="umin-sm4---asm"></a><span data-ttu-id="75632-103">Umin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="75632-103">umin (sm4 - asm)</span></span>

<span data-ttu-id="75632-104">Unsigned Integer minimo per i componenti.</span><span class="sxs-lookup"><span data-stu-id="75632-104">Component-wise unsigned integer minimum.</span></span>



| <span data-ttu-id="75632-105">Umin dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="75632-105">umin dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="75632-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="75632-106">Item</span></span>                                                            | <span data-ttu-id="75632-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75632-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="75632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="75632-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="75632-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="75632-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="75632-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="75632-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="75632-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="75632-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="75632-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="75632-113">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="75632-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="75632-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="75632-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="75632-115">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="75632-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="75632-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="75632-116">Remarks</span></span>

<span data-ttu-id="75632-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="75632-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="75632-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="75632-118">Vertex Shader</span></span> | <span data-ttu-id="75632-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="75632-119">Geometry Shader</span></span> | <span data-ttu-id="75632-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="75632-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="75632-121">x</span><span class="sxs-lookup"><span data-stu-id="75632-121">x</span></span>             | <span data-ttu-id="75632-122">x</span><span class="sxs-lookup"><span data-stu-id="75632-122">x</span></span>               | <span data-ttu-id="75632-123">x</span><span class="sxs-lookup"><span data-stu-id="75632-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="75632-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="75632-124">Minimum Shader Model</span></span>

<span data-ttu-id="75632-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="75632-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="75632-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="75632-126">Shader Model</span></span>                                              | <span data-ttu-id="75632-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="75632-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="75632-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="75632-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="75632-129">sì</span><span class="sxs-lookup"><span data-stu-id="75632-129">yes</span></span>       |
| [<span data-ttu-id="75632-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="75632-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="75632-131">sì</span><span class="sxs-lookup"><span data-stu-id="75632-131">yes</span></span>       |
| [<span data-ttu-id="75632-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="75632-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="75632-133">sì</span><span class="sxs-lookup"><span data-stu-id="75632-133">yes</span></span>       |
| [<span data-ttu-id="75632-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75632-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="75632-135">no</span><span class="sxs-lookup"><span data-stu-id="75632-135">no</span></span>        |
| [<span data-ttu-id="75632-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75632-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="75632-137">no</span><span class="sxs-lookup"><span data-stu-id="75632-137">no</span></span>        |
| [<span data-ttu-id="75632-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75632-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="75632-139">no</span><span class="sxs-lookup"><span data-stu-id="75632-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="75632-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75632-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75632-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75632-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





