---
title: IEQ (SM4-ASM)
description: Confronto di uguaglianza di interi vettori per componente.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993173"
---
# <a name="ieq-sm4---asm"></a><span data-ttu-id="86213-103">IEQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="86213-103">ieq (sm4 - asm)</span></span>

<span data-ttu-id="86213-104">Confronto di uguaglianza di interi vettori per componente.</span><span class="sxs-lookup"><span data-stu-id="86213-104">Component-wise vector integer equality comparison.</span></span>



| <span data-ttu-id="86213-105">dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="86213-105">dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="86213-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="86213-106">Item</span></span>                                                            | <span data-ttu-id="86213-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86213-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="86213-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="86213-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="86213-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="86213-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="86213-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="86213-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="86213-111">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="86213-111">\[in\] The value to compare with *src1*.</span></span><br/>           |
| <span data-ttu-id="86213-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="86213-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="86213-113">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="86213-113">\[in\] The value to compare with *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="86213-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86213-114">Remarks</span></span>

<span data-ttu-id="86213-115">Questa istruzione esegue il confronto di valori interi (*src0*  ==  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="86213-115">This instruction performs the integer comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="86213-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="86213-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="86213-117">In caso contrario, viene restituito 0x0000000</span><span class="sxs-lookup"><span data-stu-id="86213-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="86213-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="86213-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="86213-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="86213-119">Vertex Shader</span></span> | <span data-ttu-id="86213-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="86213-120">Geometry Shader</span></span> | <span data-ttu-id="86213-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="86213-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="86213-122">x</span><span class="sxs-lookup"><span data-stu-id="86213-122">x</span></span>             | <span data-ttu-id="86213-123">x</span><span class="sxs-lookup"><span data-stu-id="86213-123">x</span></span>               | <span data-ttu-id="86213-124">x</span><span class="sxs-lookup"><span data-stu-id="86213-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="86213-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="86213-125">Minimum Shader Model</span></span>

<span data-ttu-id="86213-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="86213-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="86213-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="86213-127">Shader Model</span></span>                                              | <span data-ttu-id="86213-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="86213-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="86213-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="86213-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="86213-130">sì</span><span class="sxs-lookup"><span data-stu-id="86213-130">yes</span></span>       |
| [<span data-ttu-id="86213-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="86213-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="86213-132">sì</span><span class="sxs-lookup"><span data-stu-id="86213-132">yes</span></span>       |
| [<span data-ttu-id="86213-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="86213-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="86213-134">sì</span><span class="sxs-lookup"><span data-stu-id="86213-134">yes</span></span>       |
| [<span data-ttu-id="86213-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86213-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="86213-136">no</span><span class="sxs-lookup"><span data-stu-id="86213-136">no</span></span>        |
| [<span data-ttu-id="86213-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86213-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="86213-138">no</span><span class="sxs-lookup"><span data-stu-id="86213-138">no</span></span>        |
| [<span data-ttu-id="86213-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86213-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="86213-140">no</span><span class="sxs-lookup"><span data-stu-id="86213-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="86213-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86213-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86213-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86213-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





