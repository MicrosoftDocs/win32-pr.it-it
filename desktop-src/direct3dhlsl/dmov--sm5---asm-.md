---
title: dmov (SM5-ASM)
description: Spostamento a livello di componente. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969278"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="bd52f-104">dmov (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bd52f-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="bd52f-105">Spostamento a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="bd52f-105">Component-wise move.</span></span>



| <span data-ttu-id="bd52f-106">dmov \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bd52f-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="bd52f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bd52f-107">Item</span></span>                                                            | <span data-ttu-id="bd52f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd52f-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="bd52f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bd52f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bd52f-110">\[nella \] destinazione di spostamento.</span><span class="sxs-lookup"><span data-stu-id="bd52f-110">\[in\] The move destination.</span></span> <span data-ttu-id="bd52f-111">*dest*  =  *src0*.</span><span class="sxs-lookup"><span data-stu-id="bd52f-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="bd52f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bd52f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bd52f-113">\[nei \] componenti da spostare.</span><span class="sxs-lookup"><span data-stu-id="bd52f-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="bd52f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd52f-114">Remarks</span></span>

<span data-ttu-id="bd52f-115">I modificatori, diversi da Swizzle, presuppongono che i dati siano a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="bd52f-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="bd52f-116">L'assenza di modificatori sposta i dati senza alterare i bit.</span><span class="sxs-lookup"><span data-stu-id="bd52f-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="bd52f-117">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="bd52f-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="bd52f-118">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="bd52f-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="bd52f-119">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="bd52f-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="bd52f-120">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="bd52f-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="bd52f-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd52f-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bd52f-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="bd52f-122">Vertex</span></span> | <span data-ttu-id="bd52f-123">Hull</span><span class="sxs-lookup"><span data-stu-id="bd52f-123">Hull</span></span> | <span data-ttu-id="bd52f-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="bd52f-124">Domain</span></span> | <span data-ttu-id="bd52f-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="bd52f-125">Geometry</span></span> | <span data-ttu-id="bd52f-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="bd52f-126">Pixel</span></span> | <span data-ttu-id="bd52f-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="bd52f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bd52f-128">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-128">X</span></span>      | <span data-ttu-id="bd52f-129">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-129">X</span></span>    | <span data-ttu-id="bd52f-130">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-130">X</span></span>      | <span data-ttu-id="bd52f-131">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-131">X</span></span>        | <span data-ttu-id="bd52f-132">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-132">X</span></span>     | <span data-ttu-id="bd52f-133">X</span><span class="sxs-lookup"><span data-stu-id="bd52f-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bd52f-134">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bd52f-134">Minimum Shader Model</span></span>

<span data-ttu-id="bd52f-135">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd52f-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bd52f-136">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bd52f-136">Shader Model</span></span>                                              | <span data-ttu-id="bd52f-137">Supportato</span><span class="sxs-lookup"><span data-stu-id="bd52f-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bd52f-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bd52f-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bd52f-139">sì</span><span class="sxs-lookup"><span data-stu-id="bd52f-139">yes</span></span>       |
| [<span data-ttu-id="bd52f-140">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="bd52f-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bd52f-141">no</span><span class="sxs-lookup"><span data-stu-id="bd52f-141">no</span></span>        |
| [<span data-ttu-id="bd52f-142">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="bd52f-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bd52f-143">no</span><span class="sxs-lookup"><span data-stu-id="bd52f-143">no</span></span>        |
| [<span data-ttu-id="bd52f-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bd52f-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bd52f-145">no</span><span class="sxs-lookup"><span data-stu-id="bd52f-145">no</span></span>        |
| [<span data-ttu-id="bd52f-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bd52f-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bd52f-147">no</span><span class="sxs-lookup"><span data-stu-id="bd52f-147">no</span></span>        |
| [<span data-ttu-id="bd52f-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bd52f-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bd52f-149">no</span><span class="sxs-lookup"><span data-stu-id="bd52f-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bd52f-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd52f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd52f-151">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bd52f-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





