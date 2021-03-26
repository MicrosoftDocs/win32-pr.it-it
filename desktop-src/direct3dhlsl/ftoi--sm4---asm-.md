---
title: 'ftoi (sm4 - asm) '
description: Conversione da virgola mobile a Signed Integer.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/17/2020
ms.locfileid: "104339519"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="07b9e-103">ftoi (sm4 - asm) </span><span class="sxs-lookup"><span data-stu-id="07b9e-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="07b9e-104">Conversione da virgola mobile a Signed Integer.</span><span class="sxs-lookup"><span data-stu-id="07b9e-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="07b9e-105">Ftoi dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="07b9e-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="07b9e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="07b9e-106">Item</span></span> | <span data-ttu-id="07b9e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07b9e-107">Description</span></span> |
|-|-|
| <span data-ttu-id="07b9e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="07b9e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="07b9e-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="07b9e-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="07b9e-110">*dest*  =  [round \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="07b9e-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="07b9e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="07b9e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="07b9e-112">\[nel \] componente da convertire.</span><span class="sxs-lookup"><span data-stu-id="07b9e-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="07b9e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="07b9e-113">Remarks</span></span>

<span data-ttu-id="07b9e-114">La conversione viene eseguita per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="07b9e-114">The conversion is performed per component.</span></span> <span data-ttu-id="07b9e-115">L'arrotondamento viene sempre eseguito verso zero, dopo la convenzione C per i cast da float a int. Le applicazioni che richiedono una semantica di arrotondamento diversa possono richiamare le istruzioni **round** prima di eseguire il cast su Integer.</span><span class="sxs-lookup"><span data-stu-id="07b9e-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="07b9e-116">Gli input vengono bloccati nell'intervallo \[ -2147483648.999 f... 2147483647.999 f \] prima della conversione e i valori NaN di input producono un risultato pari a zero.</span><span class="sxs-lookup"><span data-stu-id="07b9e-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="07b9e-117">I modificatori di valore assoluto e negazione facoltativi vengono applicati ai valori di origine prima della conversione.</span><span class="sxs-lookup"><span data-stu-id="07b9e-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="07b9e-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="07b9e-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="07b9e-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="07b9e-119">Vertex Shader</span></span> | <span data-ttu-id="07b9e-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="07b9e-120">Geometry Shader</span></span> | <span data-ttu-id="07b9e-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="07b9e-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="07b9e-122">x</span><span class="sxs-lookup"><span data-stu-id="07b9e-122">x</span></span> | <span data-ttu-id="07b9e-123">x</span><span class="sxs-lookup"><span data-stu-id="07b9e-123">x</span></span> | <span data-ttu-id="07b9e-124">x</span><span class="sxs-lookup"><span data-stu-id="07b9e-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="07b9e-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="07b9e-125">Minimum Shader Model</span></span>

<span data-ttu-id="07b9e-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="07b9e-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="07b9e-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="07b9e-127">Shader Model</span></span> | <span data-ttu-id="07b9e-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="07b9e-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="07b9e-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="07b9e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="07b9e-130">sì</span><span class="sxs-lookup"><span data-stu-id="07b9e-130">yes</span></span> |
| [<span data-ttu-id="07b9e-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="07b9e-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="07b9e-132">sì</span><span class="sxs-lookup"><span data-stu-id="07b9e-132">yes</span></span> |
| [<span data-ttu-id="07b9e-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="07b9e-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="07b9e-134">sì</span><span class="sxs-lookup"><span data-stu-id="07b9e-134">yes</span></span> |
| [<span data-ttu-id="07b9e-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07b9e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="07b9e-136">no</span><span class="sxs-lookup"><span data-stu-id="07b9e-136">no</span></span> |
| [<span data-ttu-id="07b9e-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07b9e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="07b9e-138">no</span><span class="sxs-lookup"><span data-stu-id="07b9e-138">no</span></span> |
| [<span data-ttu-id="07b9e-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07b9e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="07b9e-140">no</span><span class="sxs-lookup"><span data-stu-id="07b9e-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="07b9e-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07b9e-141">Related topics</span></span>

[<span data-ttu-id="07b9e-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07b9e-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
