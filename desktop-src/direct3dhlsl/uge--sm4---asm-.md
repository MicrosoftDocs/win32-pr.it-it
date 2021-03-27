---
title: uge (SM4-ASM)
description: Il vettore Component-Wise Unsigned Integer il confronto maggiore di o uguale a.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4aecd9e39aa94c69acefff0f6a0fdf843cec5d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857766"
---
# <a name="uge-sm4---asm"></a><span data-ttu-id="d68bb-103">uge (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d68bb-103">uge (sm4 - asm)</span></span>

<span data-ttu-id="d68bb-104">Il vettore Component-Wise Unsigned Integer il confronto maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="d68bb-104">Component-wise vector unsigned integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="d68bb-105">uge dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d68bb-105">uge dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="d68bb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d68bb-106">Item</span></span>                                                            | <span data-ttu-id="d68bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d68bb-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d68bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d68bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d68bb-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d68bb-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="d68bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d68bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d68bb-111">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="d68bb-111">\[in\] The components to compare to *src1*.</span></span><br/>        |
| <span data-ttu-id="d68bb-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d68bb-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d68bb-113">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d68bb-113">\[in\] The components to compare to *src0*.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="d68bb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d68bb-114">Remarks</span></span>

<span data-ttu-id="d68bb-115">Questa istruzione esegue il confronto unsigned integer (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="d68bb-115">This instruction performs the unsigned integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="d68bb-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="d68bb-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="d68bb-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d68bb-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="d68bb-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d68bb-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d68bb-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="d68bb-119">Vertex Shader</span></span> | <span data-ttu-id="d68bb-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="d68bb-120">Geometry Shader</span></span> | <span data-ttu-id="d68bb-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="d68bb-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d68bb-122">x</span><span class="sxs-lookup"><span data-stu-id="d68bb-122">x</span></span>             | <span data-ttu-id="d68bb-123">x</span><span class="sxs-lookup"><span data-stu-id="d68bb-123">x</span></span>               | <span data-ttu-id="d68bb-124">x</span><span class="sxs-lookup"><span data-stu-id="d68bb-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d68bb-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d68bb-125">Minimum Shader Model</span></span>

<span data-ttu-id="d68bb-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d68bb-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d68bb-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d68bb-127">Shader Model</span></span>                                              | <span data-ttu-id="d68bb-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="d68bb-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d68bb-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d68bb-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d68bb-130">sì</span><span class="sxs-lookup"><span data-stu-id="d68bb-130">yes</span></span>       |
| [<span data-ttu-id="d68bb-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="d68bb-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d68bb-132">sì</span><span class="sxs-lookup"><span data-stu-id="d68bb-132">yes</span></span>       |
| [<span data-ttu-id="d68bb-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d68bb-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d68bb-134">sì</span><span class="sxs-lookup"><span data-stu-id="d68bb-134">yes</span></span>       |
| [<span data-ttu-id="d68bb-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d68bb-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d68bb-136">no</span><span class="sxs-lookup"><span data-stu-id="d68bb-136">no</span></span>        |
| [<span data-ttu-id="d68bb-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d68bb-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d68bb-138">no</span><span class="sxs-lookup"><span data-stu-id="d68bb-138">no</span></span>        |
| [<span data-ttu-id="d68bb-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d68bb-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d68bb-140">no</span><span class="sxs-lookup"><span data-stu-id="d68bb-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d68bb-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d68bb-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d68bb-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d68bb-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





