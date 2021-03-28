---
title: dtof (SM5-ASM)
description: Conversione per componenti da dati a virgola mobile a precisione doppia a dati a virgola mobile a precisione singola.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335463"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="3fc56-103">dtof (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3fc56-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="3fc56-104">Conversione per componenti da dati a virgola mobile a precisione doppia a dati a virgola mobile a precisione singola.</span><span class="sxs-lookup"><span data-stu-id="3fc56-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="3fc56-105">dtof dest \[ . mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3fc56-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="3fc56-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fc56-106">Item</span></span>                                                            | <span data-ttu-id="3fc56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fc56-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fc56-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3fc56-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3fc56-109">\[nell' \] indirizzo dei dati convertiti.</span><span class="sxs-lookup"><span data-stu-id="3fc56-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="3fc56-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3fc56-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3fc56-111">\[nei \] dati da convertire.</span><span class="sxs-lookup"><span data-stu-id="3fc56-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="3fc56-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fc56-112">Remarks</span></span>

<span data-ttu-id="3fc56-113">Ogni componente dell'origine viene convertito dalla rappresentazione a precisione doppia alla rappresentazione a precisione singola usando l'arrotondamento arrotondato per eccesso.</span><span class="sxs-lookup"><span data-stu-id="3fc56-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="3fc56-114">Il valore di swizzles valido per il parametro di origine è xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="3fc56-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="3fc56-115">Le maschere *dest* valide sono uno o due componenti.</span><span class="sxs-lookup"><span data-stu-id="3fc56-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="3fc56-116">Ovvero:. x,. y,. z,. w,. XY,. xz,. XW,. YZ,. YW,. ZW il risultato della prima conversione passa al primo componente nella maschera e il risultato del secondo componente viene inserito nel secondo componente della maschera, se presente.</span><span class="sxs-lookup"><span data-stu-id="3fc56-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="3fc56-117">i componenti *dest* sono float32.</span><span class="sxs-lookup"><span data-stu-id="3fc56-117">*dest* components are float32.</span></span>

<span data-ttu-id="3fc56-118">*src* è una doppia vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB) Post Swizzle.</span><span class="sxs-lookup"><span data-stu-id="3fc56-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="3fc56-119">Per le conversioni float32<->doppie, le implementazioni possono rispettare le denormazioni di float32 o scaricarle.</span><span class="sxs-lookup"><span data-stu-id="3fc56-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="3fc56-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fc56-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3fc56-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="3fc56-121">Vertex</span></span> | <span data-ttu-id="3fc56-122">Hull</span><span class="sxs-lookup"><span data-stu-id="3fc56-122">Hull</span></span> | <span data-ttu-id="3fc56-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="3fc56-123">Domain</span></span> | <span data-ttu-id="3fc56-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="3fc56-124">Geometry</span></span> | <span data-ttu-id="3fc56-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="3fc56-125">Pixel</span></span> | <span data-ttu-id="3fc56-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3fc56-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3fc56-127">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-127">X</span></span>      | <span data-ttu-id="3fc56-128">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-128">X</span></span>    | <span data-ttu-id="3fc56-129">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-129">X</span></span>      | <span data-ttu-id="3fc56-130">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-130">X</span></span>        | <span data-ttu-id="3fc56-131">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-131">X</span></span>     | <span data-ttu-id="3fc56-132">X</span><span class="sxs-lookup"><span data-stu-id="3fc56-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3fc56-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3fc56-133">Minimum Shader Model</span></span>

<span data-ttu-id="3fc56-134">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fc56-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3fc56-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3fc56-135">Shader Model</span></span>                                              | <span data-ttu-id="3fc56-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="3fc56-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3fc56-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3fc56-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3fc56-138">sì</span><span class="sxs-lookup"><span data-stu-id="3fc56-138">yes</span></span>       |
| [<span data-ttu-id="3fc56-139">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3fc56-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3fc56-140">no</span><span class="sxs-lookup"><span data-stu-id="3fc56-140">no</span></span>        |
| [<span data-ttu-id="3fc56-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3fc56-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3fc56-142">no</span><span class="sxs-lookup"><span data-stu-id="3fc56-142">no</span></span>        |
| [<span data-ttu-id="3fc56-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fc56-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3fc56-144">no</span><span class="sxs-lookup"><span data-stu-id="3fc56-144">no</span></span>        |
| [<span data-ttu-id="3fc56-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fc56-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3fc56-146">no</span><span class="sxs-lookup"><span data-stu-id="3fc56-146">no</span></span>        |
| [<span data-ttu-id="3fc56-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fc56-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3fc56-148">no</span><span class="sxs-lookup"><span data-stu-id="3fc56-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3fc56-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fc56-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fc56-150">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fc56-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





