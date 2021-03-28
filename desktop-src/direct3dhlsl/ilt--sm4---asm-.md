---
title: ILT (SM4-ASM)
description: Confronto di un numero intero di vettori a livello di componente.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335471"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="347f4-103">ILT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="347f4-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="347f4-104">Confronto di un numero intero di vettori a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="347f4-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="347f4-105">ILT dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="347f4-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="347f4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="347f4-106">Item</span></span>                                                            | <span data-ttu-id="347f4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="347f4-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="347f4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="347f4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="347f4-109">Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="347f4-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="347f4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="347f4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="347f4-111">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="347f4-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="347f4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="347f4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="347f4-113">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="347f4-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="347f4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="347f4-114">Remarks</span></span>

<span data-ttu-id="347f4-115">Esegue il confronto di interi *(src0*  <  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="347f4-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="347f4-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="347f4-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="347f4-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="347f4-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="347f4-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="347f4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="347f4-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="347f4-119">Vertex Shader</span></span> | <span data-ttu-id="347f4-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="347f4-120">Geometry Shader</span></span> | <span data-ttu-id="347f4-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="347f4-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="347f4-122">x</span><span class="sxs-lookup"><span data-stu-id="347f4-122">x</span></span>             | <span data-ttu-id="347f4-123">x</span><span class="sxs-lookup"><span data-stu-id="347f4-123">x</span></span>               | <span data-ttu-id="347f4-124">x</span><span class="sxs-lookup"><span data-stu-id="347f4-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="347f4-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="347f4-125">Minimum Shader Model</span></span>



| <span data-ttu-id="347f4-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="347f4-126">Shader Model</span></span>                                              | <span data-ttu-id="347f4-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="347f4-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="347f4-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="347f4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="347f4-129">sì</span><span class="sxs-lookup"><span data-stu-id="347f4-129">yes</span></span>       |
| [<span data-ttu-id="347f4-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="347f4-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="347f4-131">sì</span><span class="sxs-lookup"><span data-stu-id="347f4-131">yes</span></span>       |
| [<span data-ttu-id="347f4-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="347f4-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="347f4-133">sì</span><span class="sxs-lookup"><span data-stu-id="347f4-133">yes</span></span>       |
| [<span data-ttu-id="347f4-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="347f4-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="347f4-135">no</span><span class="sxs-lookup"><span data-stu-id="347f4-135">no</span></span>        |
| [<span data-ttu-id="347f4-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="347f4-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="347f4-137">no</span><span class="sxs-lookup"><span data-stu-id="347f4-137">no</span></span>        |
| [<span data-ttu-id="347f4-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="347f4-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="347f4-139">no</span><span class="sxs-lookup"><span data-stu-id="347f4-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="347f4-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="347f4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="347f4-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="347f4-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





