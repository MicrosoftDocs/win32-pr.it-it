---
title: ftod (SM5-ASM)
description: Conversione per componente da dati a virgola mobile a precisione singola a dati a virgola mobile a precisione doppia.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335567"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="faab9-103">ftod (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="faab9-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="faab9-104">Conversione per componente da dati a virgola mobile a precisione singola a dati a virgola mobile a precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="faab9-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="faab9-105">ftod dest \[ . mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="faab9-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="faab9-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="faab9-106">Item</span></span>                                                            | <span data-ttu-id="faab9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faab9-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="faab9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="faab9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="faab9-109">\[nell' \] indirizzo dei dati convertiti.</span><span class="sxs-lookup"><span data-stu-id="faab9-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="faab9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="faab9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="faab9-111">\[nei \] dati da convertire.</span><span class="sxs-lookup"><span data-stu-id="faab9-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="faab9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="faab9-112">Remarks</span></span>

<span data-ttu-id="faab9-113">Ogni componente dell'origine viene convertito dalla rappresentazione con precisione singola alla rappresentazione a precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="faab9-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="faab9-114">Le maschere *dest* valide sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="faab9-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="faab9-115">. XY riceve il risultato della prima conversione e. ZW riceve il risultato della seconda conversione.</span><span class="sxs-lookup"><span data-stu-id="faab9-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="faab9-116">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="faab9-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="faab9-117">*src* è un vec2 float tra x e y (ZW ignorato) (post swizzle).</span><span class="sxs-lookup"><span data-stu-id="faab9-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="faab9-118">Per le conversioni float32<->doppie, le implementazioni possono rispettare le denormazioni di float32 o scaricarle.</span><span class="sxs-lookup"><span data-stu-id="faab9-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="faab9-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="faab9-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="faab9-120">Vertice</span><span class="sxs-lookup"><span data-stu-id="faab9-120">Vertex</span></span> | <span data-ttu-id="faab9-121">Hull</span><span class="sxs-lookup"><span data-stu-id="faab9-121">Hull</span></span> | <span data-ttu-id="faab9-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="faab9-122">Domain</span></span> | <span data-ttu-id="faab9-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="faab9-123">Geometry</span></span> | <span data-ttu-id="faab9-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="faab9-124">Pixel</span></span> | <span data-ttu-id="faab9-125">Calcolo</span><span class="sxs-lookup"><span data-stu-id="faab9-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="faab9-126">X</span><span class="sxs-lookup"><span data-stu-id="faab9-126">X</span></span>      | <span data-ttu-id="faab9-127">X</span><span class="sxs-lookup"><span data-stu-id="faab9-127">X</span></span>    | <span data-ttu-id="faab9-128">X</span><span class="sxs-lookup"><span data-stu-id="faab9-128">X</span></span>      | <span data-ttu-id="faab9-129">X</span><span class="sxs-lookup"><span data-stu-id="faab9-129">X</span></span>        | <span data-ttu-id="faab9-130">X</span><span class="sxs-lookup"><span data-stu-id="faab9-130">X</span></span>     | <span data-ttu-id="faab9-131">X</span><span class="sxs-lookup"><span data-stu-id="faab9-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="faab9-132">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="faab9-132">Minimum Shader Model</span></span>

<span data-ttu-id="faab9-133">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="faab9-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="faab9-134">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="faab9-134">Shader Model</span></span>                                              | <span data-ttu-id="faab9-135">Supportato</span><span class="sxs-lookup"><span data-stu-id="faab9-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="faab9-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="faab9-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="faab9-137">sì</span><span class="sxs-lookup"><span data-stu-id="faab9-137">yes</span></span>       |
| [<span data-ttu-id="faab9-138">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="faab9-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="faab9-139">no</span><span class="sxs-lookup"><span data-stu-id="faab9-139">no</span></span>        |
| [<span data-ttu-id="faab9-140">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="faab9-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="faab9-141">no</span><span class="sxs-lookup"><span data-stu-id="faab9-141">no</span></span>        |
| [<span data-ttu-id="faab9-142">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faab9-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="faab9-143">no</span><span class="sxs-lookup"><span data-stu-id="faab9-143">no</span></span>        |
| [<span data-ttu-id="faab9-144">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faab9-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="faab9-145">no</span><span class="sxs-lookup"><span data-stu-id="faab9-145">no</span></span>        |
| [<span data-ttu-id="faab9-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faab9-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="faab9-147">no</span><span class="sxs-lookup"><span data-stu-id="faab9-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="faab9-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faab9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faab9-149">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faab9-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





