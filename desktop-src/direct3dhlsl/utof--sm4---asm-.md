---
title: UTOF (SM4-ASM)
description: Intero senza segno alla conversione a virgola mobile.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046118"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="8aeca-103">UTOF (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8aeca-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="8aeca-104">Intero senza segno alla conversione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="8aeca-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="8aeca-105">UTOF dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8aeca-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="8aeca-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8aeca-106">Item</span></span>                                                            | <span data-ttu-id="8aeca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aeca-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8aeca-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8aeca-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8aeca-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8aeca-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="8aeca-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8aeca-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8aeca-111">\[nei \] componenti da convertire.</span><span class="sxs-lookup"><span data-stu-id="8aeca-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8aeca-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aeca-112">Remarks</span></span>

<span data-ttu-id="8aeca-113">*src0* deve contenere una tupla a 4 bit senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8aeca-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="8aeca-114">Dopo l'esecuzione dell'istruzione, *dest* conterrà una tupla a virgola mobile a 4 elementi.</span><span class="sxs-lookup"><span data-stu-id="8aeca-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="8aeca-115">La conversione viene eseguita per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="8aeca-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="8aeca-116">Quando un valore di input di tipo Integer è troppo grande per essere rappresentato esattamente nel formato a virgola mobile, arrotondare alla modalità pari più vicina.</span><span class="sxs-lookup"><span data-stu-id="8aeca-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="8aeca-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8aeca-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8aeca-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="8aeca-118">Vertex Shader</span></span> | <span data-ttu-id="8aeca-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="8aeca-119">Geometry Shader</span></span> | <span data-ttu-id="8aeca-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="8aeca-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8aeca-121">x</span><span class="sxs-lookup"><span data-stu-id="8aeca-121">x</span></span>             | <span data-ttu-id="8aeca-122">x</span><span class="sxs-lookup"><span data-stu-id="8aeca-122">x</span></span>               | <span data-ttu-id="8aeca-123">x</span><span class="sxs-lookup"><span data-stu-id="8aeca-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8aeca-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8aeca-124">Minimum Shader Model</span></span>

<span data-ttu-id="8aeca-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8aeca-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8aeca-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8aeca-126">Shader Model</span></span>                                              | <span data-ttu-id="8aeca-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="8aeca-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8aeca-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8aeca-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8aeca-129">sì</span><span class="sxs-lookup"><span data-stu-id="8aeca-129">yes</span></span>       |
| [<span data-ttu-id="8aeca-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8aeca-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8aeca-131">sì</span><span class="sxs-lookup"><span data-stu-id="8aeca-131">yes</span></span>       |
| [<span data-ttu-id="8aeca-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8aeca-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8aeca-133">sì</span><span class="sxs-lookup"><span data-stu-id="8aeca-133">yes</span></span>       |
| [<span data-ttu-id="8aeca-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8aeca-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8aeca-135">no</span><span class="sxs-lookup"><span data-stu-id="8aeca-135">no</span></span>        |
| [<span data-ttu-id="8aeca-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8aeca-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8aeca-137">no</span><span class="sxs-lookup"><span data-stu-id="8aeca-137">no</span></span>        |
| [<span data-ttu-id="8aeca-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8aeca-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8aeca-139">no</span><span class="sxs-lookup"><span data-stu-id="8aeca-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8aeca-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8aeca-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aeca-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8aeca-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





