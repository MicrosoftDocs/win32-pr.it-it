---
title: itof (SM4-ASM)
description: Intero con segno alla conversione a virgola mobile.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857782"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="80eae-103">itof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="80eae-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="80eae-104">Intero con segno alla conversione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="80eae-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="80eae-105">itof dest \[ . mask \] , \[ - \] src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="80eae-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="80eae-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="80eae-106">Item</span></span>                                                            | <span data-ttu-id="80eae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80eae-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="80eae-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="80eae-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="80eae-109">\[in \] contiene il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="80eae-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="80eae-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="80eae-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="80eae-111">\[in \] contiene il valore da convertire.</span><span class="sxs-lookup"><span data-stu-id="80eae-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="80eae-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="80eae-112">Remarks</span></span>

<span data-ttu-id="80eae-113">Questa istruzione di conversione da Integer a float con segno presuppone che *src0* contenga una tupla con valore intero a 32 bit con segno 4.</span><span class="sxs-lookup"><span data-stu-id="80eae-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="80eae-114">Dopo l'esecuzione dell'istruzione, *dest* conterrà una tupla a virgola mobile a 4 elementi.</span><span class="sxs-lookup"><span data-stu-id="80eae-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="80eae-115">La conversione viene eseguita per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="80eae-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="80eae-116">Quando un valore di input di tipo Integer è troppo grande per essere rappresentato esattamente nel formato a virgola mobile, l'arrotondamento alla modalità pari più vicina è fortemente consigliato ma non obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80eae-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="80eae-117">Il modificatore negazioni facoltativo nell'operando di origine accetta il complemento di 2 prima di eseguire un'operazione aritmetica.</span><span class="sxs-lookup"><span data-stu-id="80eae-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="80eae-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="80eae-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80eae-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="80eae-119">Vertex Shader</span></span> | <span data-ttu-id="80eae-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="80eae-120">Geometry Shader</span></span> | <span data-ttu-id="80eae-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="80eae-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="80eae-122">x</span><span class="sxs-lookup"><span data-stu-id="80eae-122">x</span></span>             | <span data-ttu-id="80eae-123">x</span><span class="sxs-lookup"><span data-stu-id="80eae-123">x</span></span>               | <span data-ttu-id="80eae-124">x</span><span class="sxs-lookup"><span data-stu-id="80eae-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="80eae-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="80eae-125">Minimum Shader Model</span></span>

<span data-ttu-id="80eae-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="80eae-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80eae-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="80eae-127">Shader Model</span></span>                                              | <span data-ttu-id="80eae-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="80eae-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80eae-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="80eae-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80eae-130">sì</span><span class="sxs-lookup"><span data-stu-id="80eae-130">yes</span></span>       |
| [<span data-ttu-id="80eae-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="80eae-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80eae-132">sì</span><span class="sxs-lookup"><span data-stu-id="80eae-132">yes</span></span>       |
| [<span data-ttu-id="80eae-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="80eae-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80eae-134">sì</span><span class="sxs-lookup"><span data-stu-id="80eae-134">yes</span></span>       |
| [<span data-ttu-id="80eae-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80eae-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80eae-136">no</span><span class="sxs-lookup"><span data-stu-id="80eae-136">no</span></span>        |
| [<span data-ttu-id="80eae-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80eae-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80eae-138">no</span><span class="sxs-lookup"><span data-stu-id="80eae-138">no</span></span>        |
| [<span data-ttu-id="80eae-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80eae-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80eae-140">no</span><span class="sxs-lookup"><span data-stu-id="80eae-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80eae-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80eae-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80eae-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80eae-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





