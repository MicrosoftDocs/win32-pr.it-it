---
title: dne (SM5-ASM)
description: Confronto di uguaglianza a precisione doppia a livello di componente.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae00e0e5f4c0269b14a7a0f330d5af8760a1312f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398249"
---
# <a name="dne-sm5---asm"></a><span data-ttu-id="e2e68-103">dne (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e2e68-103">dne (sm5 - asm)</span></span>

<span data-ttu-id="e2e68-104">Confronto di uguaglianza a precisione doppia a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="e2e68-104">Component-wise double-precision not equality comparison.</span></span>



| <span data-ttu-id="e2e68-105">dne \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e2e68-105">dne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e2e68-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e2e68-106">Item</span></span>                                                            | <span data-ttu-id="e2e68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2e68-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e2e68-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e2e68-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e2e68-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e2e68-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e2e68-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e2e68-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e2e68-111">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="e2e68-111">\[in\] The components to compare with *src1*.</span></span><br/>      |
| <span data-ttu-id="e2e68-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e2e68-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e2e68-113">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="e2e68-113">\[in\] The components to compare with *src0*.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e2e68-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2e68-114">Remarks</span></span>

<span data-ttu-id="e2e68-115">Questa istruzione esegue il confronto a virgola mobile a precisione doppia (*src0* ! = *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="e2e68-115">This instruction performs the double-precision floating-point comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="e2e68-116">Se il confronto è true, viene restituito 0xFFFFFFFF a 32 bit per quel componente.</span><span class="sxs-lookup"><span data-stu-id="e2e68-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="e2e68-117">In caso contrario, viene restituito 0x00000000 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e2e68-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="e2e68-118">Il confronto con NaN restituisce true.</span><span class="sxs-lookup"><span data-stu-id="e2e68-118">Comparison with NaN returns true.</span></span>

<span data-ttu-id="e2e68-119">Le maschere *dest* valide sono uno o due componenti.</span><span class="sxs-lookup"><span data-stu-id="e2e68-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="e2e68-120">Ovvero:. x,. y,. z,. w,. XY,. xz,. XW,. YZ,. YW,. ZW il primo componente *dest* nella maschera riceve il risultato 32 bit per il primo doppio confronto.</span><span class="sxs-lookup"><span data-stu-id="e2e68-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="e2e68-121">Il secondo componente della maschera, se presente, riceve il risultato di 32 bit per il secondo confronto doppio.</span><span class="sxs-lookup"><span data-stu-id="e2e68-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="e2e68-122">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="e2e68-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="e2e68-123">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="e2e68-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="e2e68-124">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="e2e68-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="e2e68-125">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="e2e68-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="e2e68-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2e68-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e2e68-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="e2e68-127">Vertex</span></span> | <span data-ttu-id="e2e68-128">Hull</span><span class="sxs-lookup"><span data-stu-id="e2e68-128">Hull</span></span> | <span data-ttu-id="e2e68-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="e2e68-129">Domain</span></span> | <span data-ttu-id="e2e68-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="e2e68-130">Geometry</span></span> | <span data-ttu-id="e2e68-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="e2e68-131">Pixel</span></span> | <span data-ttu-id="e2e68-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e2e68-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e2e68-133">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-133">X</span></span>      | <span data-ttu-id="e2e68-134">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-134">X</span></span>    | <span data-ttu-id="e2e68-135">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-135">X</span></span>      | <span data-ttu-id="e2e68-136">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-136">X</span></span>        | <span data-ttu-id="e2e68-137">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-137">X</span></span>     | <span data-ttu-id="e2e68-138">X</span><span class="sxs-lookup"><span data-stu-id="e2e68-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e2e68-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e2e68-139">Minimum Shader Model</span></span>

<span data-ttu-id="e2e68-140">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2e68-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e2e68-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e2e68-141">Shader Model</span></span>                                              | <span data-ttu-id="e2e68-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="e2e68-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e2e68-143">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e2e68-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e2e68-144">sì</span><span class="sxs-lookup"><span data-stu-id="e2e68-144">yes</span></span>       |
| [<span data-ttu-id="e2e68-145">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e2e68-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e2e68-146">no</span><span class="sxs-lookup"><span data-stu-id="e2e68-146">no</span></span>        |
| [<span data-ttu-id="e2e68-147">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e2e68-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e2e68-148">no</span><span class="sxs-lookup"><span data-stu-id="e2e68-148">no</span></span>        |
| [<span data-ttu-id="e2e68-149">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2e68-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e2e68-150">no</span><span class="sxs-lookup"><span data-stu-id="e2e68-150">no</span></span>        |
| [<span data-ttu-id="e2e68-151">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2e68-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e2e68-152">no</span><span class="sxs-lookup"><span data-stu-id="e2e68-152">no</span></span>        |
| [<span data-ttu-id="e2e68-153">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2e68-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e2e68-154">no</span><span class="sxs-lookup"><span data-stu-id="e2e68-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e2e68-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2e68-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2e68-156">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2e68-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





