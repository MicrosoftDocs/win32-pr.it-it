---
title: Imin (SM4-ASM)
description: Valore minimo per componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398273"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="d69bb-103">Imin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d69bb-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="d69bb-104">Valore minimo per componente.</span><span class="sxs-lookup"><span data-stu-id="d69bb-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="d69bb-105">Imin dest \[ . mask \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d69bb-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="d69bb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d69bb-106">Item</span></span>                                                            | <span data-ttu-id="d69bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d69bb-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d69bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d69bb-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d69bb-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="d69bb-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="d69bb-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="d69bb-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="d69bb-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="d69bb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d69bb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d69bb-113">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="d69bb-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="d69bb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d69bb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d69bb-115">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d69bb-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d69bb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d69bb-116">Remarks</span></span>

<span data-ttu-id="d69bb-117">Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d69bb-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="d69bb-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d69bb-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d69bb-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="d69bb-119">Vertex Shader</span></span> | <span data-ttu-id="d69bb-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="d69bb-120">Geometry Shader</span></span> | <span data-ttu-id="d69bb-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="d69bb-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d69bb-122">x</span><span class="sxs-lookup"><span data-stu-id="d69bb-122">x</span></span>             | <span data-ttu-id="d69bb-123">x</span><span class="sxs-lookup"><span data-stu-id="d69bb-123">x</span></span>               | <span data-ttu-id="d69bb-124">x</span><span class="sxs-lookup"><span data-stu-id="d69bb-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d69bb-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d69bb-125">Minimum Shader Model</span></span>

<span data-ttu-id="d69bb-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d69bb-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d69bb-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d69bb-127">Shader Model</span></span>                                              | <span data-ttu-id="d69bb-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="d69bb-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d69bb-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d69bb-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d69bb-130">sì</span><span class="sxs-lookup"><span data-stu-id="d69bb-130">yes</span></span>       |
| [<span data-ttu-id="d69bb-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="d69bb-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d69bb-132">sì</span><span class="sxs-lookup"><span data-stu-id="d69bb-132">yes</span></span>       |
| [<span data-ttu-id="d69bb-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d69bb-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d69bb-134">sì</span><span class="sxs-lookup"><span data-stu-id="d69bb-134">yes</span></span>       |
| [<span data-ttu-id="d69bb-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d69bb-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d69bb-136">no</span><span class="sxs-lookup"><span data-stu-id="d69bb-136">no</span></span>        |
| [<span data-ttu-id="d69bb-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d69bb-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d69bb-138">no</span><span class="sxs-lookup"><span data-stu-id="d69bb-138">no</span></span>        |
| [<span data-ttu-id="d69bb-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d69bb-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d69bb-140">no</span><span class="sxs-lookup"><span data-stu-id="d69bb-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d69bb-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d69bb-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d69bb-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d69bb-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





