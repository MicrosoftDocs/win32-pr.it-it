---
title: IMAX (SM4-ASM)
description: Numero intero a livello di componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117181"
---
# <a name="imax-sm4---asm"></a><span data-ttu-id="ecc2d-103">IMAX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ecc2d-103">imax (sm4 - asm)</span></span>

<span data-ttu-id="ecc2d-104">Numero intero a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-104">Component-wise integer maximum.</span></span>



| <span data-ttu-id="ecc2d-105">dest \[ . mask IMAX \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="ecc2d-105">imax dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="ecc2d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ecc2d-106">Item</span></span>                                                            | <span data-ttu-id="ecc2d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc2d-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ecc2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ecc2d-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="ecc2d-110">*dest*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="ecc2d-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="ecc2d-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="ecc2d-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="ecc2d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ecc2d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ecc2d-113">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="ecc2d-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ecc2d-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ecc2d-115">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ecc2d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecc2d-116">Remarks</span></span>

<span data-ttu-id="ecc2d-117">Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="ecc2d-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecc2d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ecc2d-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="ecc2d-119">Vertex Shader</span></span> | <span data-ttu-id="ecc2d-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="ecc2d-120">Geometry Shader</span></span> | <span data-ttu-id="ecc2d-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="ecc2d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ecc2d-122">x</span><span class="sxs-lookup"><span data-stu-id="ecc2d-122">x</span></span>             | <span data-ttu-id="ecc2d-123">x</span><span class="sxs-lookup"><span data-stu-id="ecc2d-123">x</span></span>               | <span data-ttu-id="ecc2d-124">x</span><span class="sxs-lookup"><span data-stu-id="ecc2d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ecc2d-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ecc2d-125">Minimum Shader Model</span></span>

<span data-ttu-id="ecc2d-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ecc2d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecc2d-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ecc2d-127">Shader Model</span></span>                                              | <span data-ttu-id="ecc2d-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="ecc2d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ecc2d-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ecc2d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ecc2d-130">sì</span><span class="sxs-lookup"><span data-stu-id="ecc2d-130">yes</span></span>       |
| [<span data-ttu-id="ecc2d-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ecc2d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ecc2d-132">sì</span><span class="sxs-lookup"><span data-stu-id="ecc2d-132">yes</span></span>       |
| [<span data-ttu-id="ecc2d-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ecc2d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecc2d-134">sì</span><span class="sxs-lookup"><span data-stu-id="ecc2d-134">yes</span></span>       |
| [<span data-ttu-id="ecc2d-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc2d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecc2d-136">no</span><span class="sxs-lookup"><span data-stu-id="ecc2d-136">no</span></span>        |
| [<span data-ttu-id="ecc2d-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc2d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecc2d-138">no</span><span class="sxs-lookup"><span data-stu-id="ecc2d-138">no</span></span>        |
| [<span data-ttu-id="ecc2d-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc2d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecc2d-140">no</span><span class="sxs-lookup"><span data-stu-id="ecc2d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ecc2d-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecc2d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecc2d-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc2d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





