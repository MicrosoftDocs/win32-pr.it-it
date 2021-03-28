---
title: Bor (SM5-ASM)
description: Confronto a precisione doppia a livello di componente maggiore di o uguale a.
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508354affbabe1ebab70be31ab45f0e7f80d0765
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046068"
---
# <a name="dge-sm5---asm"></a><span data-ttu-id="ff413-103">Bor (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff413-103">dge (sm5 - asm)</span></span>

<span data-ttu-id="ff413-104">Confronto a precisione doppia a livello di componente maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="ff413-104">Component-wise double-precision greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="ff413-105">Bor \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ff413-105">dge\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ff413-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff413-106">Item</span></span>                                                            | <span data-ttu-id="ff413-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff413-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ff413-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ff413-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ff413-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ff413-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ff413-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ff413-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ff413-111">Componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="ff413-111">The components to compare to *src1*.</span></span><br/>                |
| <span data-ttu-id="ff413-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ff413-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ff413-113">Componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="ff413-113">The components to compare to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="ff413-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff413-114">Remarks</span></span>

<span data-ttu-id="ff413-115">Questa istruzione esegue il confronto a virgola mobile a precisione doppia (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="ff413-115">This instruction performs the double-precision floating-point comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="ff413-116">Se il confronto è true, viene restituito 0xFFFFFFFF a 32 bit per quel componente.</span><span class="sxs-lookup"><span data-stu-id="ff413-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="ff413-117">In caso contrario, viene restituito 0x00000000 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ff413-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="ff413-118">Il confronto con NaN restituisce false.</span><span class="sxs-lookup"><span data-stu-id="ff413-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="ff413-119">Le maschere *dest* valide sono uno o due componenti.</span><span class="sxs-lookup"><span data-stu-id="ff413-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="ff413-120">Ovvero:. x,. y,. z,. w,. XY,. xz,. XW,. YZ,. YW,. ZW il primo componente *dest* nella maschera riceve il risultato 32 bit per il primo doppio confronto.</span><span class="sxs-lookup"><span data-stu-id="ff413-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="ff413-121">Il secondo componente della maschera, se presente, riceve il risultato di 32 bit per il secondo confronto doppio.</span><span class="sxs-lookup"><span data-stu-id="ff413-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="ff413-122">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="ff413-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="ff413-123">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="ff413-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="ff413-124">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="ff413-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="ff413-125">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="ff413-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="ff413-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff413-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff413-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="ff413-127">Vertex</span></span> | <span data-ttu-id="ff413-128">Hull</span><span class="sxs-lookup"><span data-stu-id="ff413-128">Hull</span></span> | <span data-ttu-id="ff413-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="ff413-129">Domain</span></span> | <span data-ttu-id="ff413-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="ff413-130">Geometry</span></span> | <span data-ttu-id="ff413-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="ff413-131">Pixel</span></span> | <span data-ttu-id="ff413-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ff413-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ff413-133">X</span><span class="sxs-lookup"><span data-stu-id="ff413-133">X</span></span>      | <span data-ttu-id="ff413-134">X</span><span class="sxs-lookup"><span data-stu-id="ff413-134">X</span></span>    | <span data-ttu-id="ff413-135">X</span><span class="sxs-lookup"><span data-stu-id="ff413-135">X</span></span>      | <span data-ttu-id="ff413-136">X</span><span class="sxs-lookup"><span data-stu-id="ff413-136">X</span></span>        | <span data-ttu-id="ff413-137">X</span><span class="sxs-lookup"><span data-stu-id="ff413-137">X</span></span>     | <span data-ttu-id="ff413-138">X</span><span class="sxs-lookup"><span data-stu-id="ff413-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff413-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ff413-139">Minimum Shader Model</span></span>

<span data-ttu-id="ff413-140">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff413-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ff413-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ff413-141">Shader Model</span></span>                                              | <span data-ttu-id="ff413-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="ff413-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff413-143">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ff413-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff413-144">sì</span><span class="sxs-lookup"><span data-stu-id="ff413-144">yes</span></span>       |
| [<span data-ttu-id="ff413-145">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ff413-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff413-146">no</span><span class="sxs-lookup"><span data-stu-id="ff413-146">no</span></span>        |
| [<span data-ttu-id="ff413-147">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ff413-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff413-148">no</span><span class="sxs-lookup"><span data-stu-id="ff413-148">no</span></span>        |
| [<span data-ttu-id="ff413-149">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff413-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff413-150">no</span><span class="sxs-lookup"><span data-stu-id="ff413-150">no</span></span>        |
| [<span data-ttu-id="ff413-151">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff413-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff413-152">no</span><span class="sxs-lookup"><span data-stu-id="ff413-152">no</span></span>        |
| [<span data-ttu-id="ff413-153">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff413-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff413-154">no</span><span class="sxs-lookup"><span data-stu-id="ff413-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff413-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff413-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff413-156">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff413-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





