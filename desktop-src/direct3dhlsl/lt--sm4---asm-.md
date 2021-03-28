---
title: lt (SM4-ASM)
description: Confronto a virgola mobile a virgola mobile a livello di componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335527"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="b25d5-103">lt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b25d5-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="b25d5-104">Confronto a virgola mobile a virgola mobile a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="b25d5-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="b25d5-105">lt dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b25d5-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="b25d5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b25d5-106">Item</span></span>                                                            | <span data-ttu-id="b25d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b25d5-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b25d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b25d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b25d5-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b25d5-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b25d5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b25d5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b25d5-111">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="b25d5-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="b25d5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b25d5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b25d5-113">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="b25d5-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="b25d5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b25d5-114">Remarks</span></span>

<span data-ttu-id="b25d5-115">Questa istruzione esegue il confronto float (*src0*  <  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="b25d5-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="b25d5-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="b25d5-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="b25d5-117">In caso contrario, viene restituito 0x0000000</span><span class="sxs-lookup"><span data-stu-id="b25d5-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="b25d5-118">Le denormazioni vengono scaricate prima del confronto. i registri di origine originali non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="b25d5-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="b25d5-119">+ 0 è uguale a-0.</span><span class="sxs-lookup"><span data-stu-id="b25d5-119">+0 equals -0.</span></span>

<span data-ttu-id="b25d5-120">Il confronto con NaN restituisce false.</span><span class="sxs-lookup"><span data-stu-id="b25d5-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="b25d5-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b25d5-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b25d5-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="b25d5-122">Vertex Shader</span></span> | <span data-ttu-id="b25d5-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="b25d5-123">Geometry Shader</span></span> | <span data-ttu-id="b25d5-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="b25d5-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b25d5-125">x</span><span class="sxs-lookup"><span data-stu-id="b25d5-125">x</span></span>             | <span data-ttu-id="b25d5-126">x</span><span class="sxs-lookup"><span data-stu-id="b25d5-126">x</span></span>               | <span data-ttu-id="b25d5-127">x</span><span class="sxs-lookup"><span data-stu-id="b25d5-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b25d5-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b25d5-128">Minimum Shader Model</span></span>

<span data-ttu-id="b25d5-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b25d5-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b25d5-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b25d5-130">Shader Model</span></span>                                              | <span data-ttu-id="b25d5-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="b25d5-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b25d5-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b25d5-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b25d5-133">sì</span><span class="sxs-lookup"><span data-stu-id="b25d5-133">yes</span></span>       |
| [<span data-ttu-id="b25d5-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b25d5-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b25d5-135">sì</span><span class="sxs-lookup"><span data-stu-id="b25d5-135">yes</span></span>       |
| [<span data-ttu-id="b25d5-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b25d5-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b25d5-137">sì</span><span class="sxs-lookup"><span data-stu-id="b25d5-137">yes</span></span>       |
| [<span data-ttu-id="b25d5-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b25d5-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b25d5-139">no</span><span class="sxs-lookup"><span data-stu-id="b25d5-139">no</span></span>        |
| [<span data-ttu-id="b25d5-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b25d5-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b25d5-141">no</span><span class="sxs-lookup"><span data-stu-id="b25d5-141">no</span></span>        |
| [<span data-ttu-id="b25d5-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b25d5-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b25d5-143">no</span><span class="sxs-lookup"><span data-stu-id="b25d5-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b25d5-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b25d5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b25d5-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b25d5-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





