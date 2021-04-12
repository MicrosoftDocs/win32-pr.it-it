---
title: ftou (SM4-ASM)
description: Conversione da virgola mobile a Unsigned Integer.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335487"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="aaa36-103">ftou (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aaa36-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="aaa36-104">Conversione da virgola mobile a Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="aaa36-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="aaa36-105">ftou dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aaa36-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="aaa36-106">Ftoi dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aaa36-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="aaa36-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="aaa36-107">Item</span></span>                                                            | <span data-ttu-id="aaa36-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaa36-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="aaa36-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="aaa36-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="aaa36-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="aaa36-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="aaa36-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aaa36-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="aaa36-112">\[nel \] valore da convertire.</span><span class="sxs-lookup"><span data-stu-id="aaa36-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="aaa36-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaa36-113">Remarks</span></span>

<span data-ttu-id="aaa36-114">La conversione viene eseguita per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="aaa36-114">The conversion is performed per-component.</span></span> <span data-ttu-id="aaa36-115">L'arrotondamento viene sempre eseguito verso zero, dopo la convenzione C per i cast da float a int.</span><span class="sxs-lookup"><span data-stu-id="aaa36-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="aaa36-116">Le applicazioni che richiedono una semantica di arrotondamento diversa possono richiamare le istruzioni **round** prima di eseguire il cast su Integer.</span><span class="sxs-lookup"><span data-stu-id="aaa36-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="aaa36-117">Gli input vengono fissati nell'intervallo \[ 0,0 f... 4294967295.999 f \] prima della conversione e i valori NaN di input producono un risultato pari a zero.</span><span class="sxs-lookup"><span data-stu-id="aaa36-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="aaa36-118">I modificatori di valore assoluto e negazione facoltativi vengono applicati ai valori di origine prima della conversione.</span><span class="sxs-lookup"><span data-stu-id="aaa36-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="aaa36-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaa36-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aaa36-120">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="aaa36-120">Vertex Shader</span></span> | <span data-ttu-id="aaa36-121">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="aaa36-121">Geometry Shader</span></span> | <span data-ttu-id="aaa36-122">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="aaa36-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aaa36-123">x</span><span class="sxs-lookup"><span data-stu-id="aaa36-123">x</span></span>             | <span data-ttu-id="aaa36-124">x</span><span class="sxs-lookup"><span data-stu-id="aaa36-124">x</span></span>               | <span data-ttu-id="aaa36-125">x</span><span class="sxs-lookup"><span data-stu-id="aaa36-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aaa36-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="aaa36-126">Minimum Shader Model</span></span>

<span data-ttu-id="aaa36-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="aaa36-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aaa36-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="aaa36-128">Shader Model</span></span>                                              | <span data-ttu-id="aaa36-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="aaa36-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aaa36-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="aaa36-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aaa36-131">sì</span><span class="sxs-lookup"><span data-stu-id="aaa36-131">yes</span></span>       |
| [<span data-ttu-id="aaa36-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="aaa36-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aaa36-133">sì</span><span class="sxs-lookup"><span data-stu-id="aaa36-133">yes</span></span>       |
| [<span data-ttu-id="aaa36-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="aaa36-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aaa36-135">sì</span><span class="sxs-lookup"><span data-stu-id="aaa36-135">yes</span></span>       |
| [<span data-ttu-id="aaa36-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aaa36-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aaa36-137">no</span><span class="sxs-lookup"><span data-stu-id="aaa36-137">no</span></span>        |
| [<span data-ttu-id="aaa36-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aaa36-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aaa36-139">no</span><span class="sxs-lookup"><span data-stu-id="aaa36-139">no</span></span>        |
| [<span data-ttu-id="aaa36-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aaa36-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aaa36-141">no</span><span class="sxs-lookup"><span data-stu-id="aaa36-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aaa36-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaa36-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaa36-143">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aaa36-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





