---
title: Ultimate (SM4-ASM)
description: Il confronto con il vettore a livello di componente Unsigned Integer meno di.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993032"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="765f9-103">Ultimate (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="765f9-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="765f9-104">Il confronto con il vettore a livello di componente Unsigned Integer meno di.</span><span class="sxs-lookup"><span data-stu-id="765f9-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="765f9-105">Ultimate dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="765f9-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="765f9-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="765f9-106">Item</span></span>                                                            | <span data-ttu-id="765f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="765f9-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="765f9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="765f9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="765f9-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="765f9-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="765f9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="765f9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="765f9-111">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="765f9-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="765f9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="765f9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="765f9-113">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="765f9-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="765f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="765f9-114">Remarks</span></span>

<span data-ttu-id="765f9-115">Esegue il confronto unsigned integer (*src0*  <  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="765f9-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="765f9-116">Se il confronto è true, questa istruzione restituisce 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="765f9-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="765f9-117">In caso contrario, restituisce 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="765f9-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="765f9-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="765f9-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="765f9-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="765f9-119">Vertex Shader</span></span> | <span data-ttu-id="765f9-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="765f9-120">Geometry Shader</span></span> | <span data-ttu-id="765f9-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="765f9-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="765f9-122">x</span><span class="sxs-lookup"><span data-stu-id="765f9-122">x</span></span>             | <span data-ttu-id="765f9-123">x</span><span class="sxs-lookup"><span data-stu-id="765f9-123">x</span></span>               | <span data-ttu-id="765f9-124">x</span><span class="sxs-lookup"><span data-stu-id="765f9-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="765f9-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="765f9-125">Minimum Shader Model</span></span>

<span data-ttu-id="765f9-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="765f9-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="765f9-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="765f9-127">Shader Model</span></span>                                              | <span data-ttu-id="765f9-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="765f9-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="765f9-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="765f9-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="765f9-130">sì</span><span class="sxs-lookup"><span data-stu-id="765f9-130">yes</span></span>       |
| [<span data-ttu-id="765f9-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="765f9-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="765f9-132">sì</span><span class="sxs-lookup"><span data-stu-id="765f9-132">yes</span></span>       |
| [<span data-ttu-id="765f9-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="765f9-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="765f9-134">sì</span><span class="sxs-lookup"><span data-stu-id="765f9-134">yes</span></span>       |
| [<span data-ttu-id="765f9-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="765f9-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="765f9-136">no</span><span class="sxs-lookup"><span data-stu-id="765f9-136">no</span></span>        |
| [<span data-ttu-id="765f9-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="765f9-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="765f9-138">no</span><span class="sxs-lookup"><span data-stu-id="765f9-138">no</span></span>        |
| [<span data-ttu-id="765f9-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="765f9-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="765f9-140">no</span><span class="sxs-lookup"><span data-stu-id="765f9-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="765f9-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="765f9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="765f9-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="765f9-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





