---
title: ne (SM4-ASM)
description: Confronto tra punti a virgola mobile e vettore per componente.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398244"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="9bae4-103">ne (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9bae4-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="9bae4-104">Confronto tra punti a virgola mobile e vettore per componente.</span><span class="sxs-lookup"><span data-stu-id="9bae4-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="9bae4-105">ne dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9bae4-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="9bae4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9bae4-106">Item</span></span>                                                            | <span data-ttu-id="9bae4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bae4-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="9bae4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9bae4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9bae4-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9bae4-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="9bae4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9bae4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9bae4-111">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="9bae4-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="9bae4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9bae4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9bae4-113">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="9bae4-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9bae4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bae4-114">Remarks</span></span>

<span data-ttu-id="9bae4-115">Questa istruzione esegue il confronto float (*src0* ! = *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="9bae4-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="9bae4-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="9bae4-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="9bae4-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="9bae4-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="9bae4-118">Le denormazioni vengono scaricate prima del confronto con i registri di origine non modificati.</span><span class="sxs-lookup"><span data-stu-id="9bae4-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="9bae4-119">+ 0 è uguale a-0.</span><span class="sxs-lookup"><span data-stu-id="9bae4-119">+0 equals -0.</span></span>

<span data-ttu-id="9bae4-120">Il confronto con NaN restituisce true.</span><span class="sxs-lookup"><span data-stu-id="9bae4-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="9bae4-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9bae4-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9bae4-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9bae4-122">Vertex Shader</span></span> | <span data-ttu-id="9bae4-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9bae4-123">Geometry Shader</span></span> | <span data-ttu-id="9bae4-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9bae4-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9bae4-125">x</span><span class="sxs-lookup"><span data-stu-id="9bae4-125">x</span></span>             | <span data-ttu-id="9bae4-126">x</span><span class="sxs-lookup"><span data-stu-id="9bae4-126">x</span></span>               | <span data-ttu-id="9bae4-127">x</span><span class="sxs-lookup"><span data-stu-id="9bae4-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bae4-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9bae4-128">Minimum Shader Model</span></span>

<span data-ttu-id="9bae4-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bae4-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bae4-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9bae4-130">Shader Model</span></span>                                              | <span data-ttu-id="9bae4-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="9bae4-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9bae4-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9bae4-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9bae4-133">sì</span><span class="sxs-lookup"><span data-stu-id="9bae4-133">yes</span></span>       |
| [<span data-ttu-id="9bae4-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9bae4-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9bae4-135">sì</span><span class="sxs-lookup"><span data-stu-id="9bae4-135">yes</span></span>       |
| [<span data-ttu-id="9bae4-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9bae4-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bae4-137">sì</span><span class="sxs-lookup"><span data-stu-id="9bae4-137">yes</span></span>       |
| [<span data-ttu-id="9bae4-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bae4-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bae4-139">no</span><span class="sxs-lookup"><span data-stu-id="9bae4-139">no</span></span>        |
| [<span data-ttu-id="9bae4-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bae4-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bae4-141">no</span><span class="sxs-lookup"><span data-stu-id="9bae4-141">no</span></span>        |
| [<span data-ttu-id="9bae4-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bae4-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bae4-143">no</span><span class="sxs-lookup"><span data-stu-id="9bae4-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9bae4-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bae4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bae4-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bae4-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





