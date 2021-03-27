---
title: EQ (SM4-ASM)
description: Confronto di uguaglianza a virgola mobile vettoriale a livello di componente.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f47dc7bda7b1c61c251ace061fc75897788b968
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398186"
---
# <a name="eq-sm4---asm"></a><span data-ttu-id="88c53-103">EQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="88c53-103">eq (sm4 - asm)</span></span>

<span data-ttu-id="88c53-104">Confronto di uguaglianza a virgola mobile vettoriale a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="88c53-104">Component-wise vector floating point equality comparison.</span></span>



| <span data-ttu-id="88c53-105">EQ dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="88c53-105">eq dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="88c53-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="88c53-106">Item</span></span>                                                            | <span data-ttu-id="88c53-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88c53-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="88c53-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="88c53-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="88c53-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="88c53-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="88c53-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="88c53-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="88c53-111">\[nel \] componente da comapre a *src1*.</span><span class="sxs-lookup"><span data-stu-id="88c53-111">\[in\] The component to comapre to *src1*.</span></span><br/>         |
| <span data-ttu-id="88c53-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="88c53-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="88c53-113">\[nel \] componente da comapre a *src0*.</span><span class="sxs-lookup"><span data-stu-id="88c53-113">\[in\] The component to comapre to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="88c53-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="88c53-114">Remarks</span></span>

<span data-ttu-id="88c53-115">Esegue il confronto float (*src0*  ==  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="88c53-115">Performs the float comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="88c53-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="88c53-116">If the comparison is true, 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="88c53-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="88c53-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="88c53-118">Le denormazioni vengono scaricate prima del confronto (i registri di origine originali non vengono modificati).</span><span class="sxs-lookup"><span data-stu-id="88c53-118">Denorms are flushed before comparison (original source registers untouched).</span></span> <span data-ttu-id="88c53-119">+ 0 è uguale a-0.</span><span class="sxs-lookup"><span data-stu-id="88c53-119">+0 equals -0.</span></span> <span data-ttu-id="88c53-120">Il confronto con NaN restituisce false.</span><span class="sxs-lookup"><span data-stu-id="88c53-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="88c53-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="88c53-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="88c53-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="88c53-122">Vertex Shader</span></span> | <span data-ttu-id="88c53-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="88c53-123">Geometry Shader</span></span> | <span data-ttu-id="88c53-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="88c53-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="88c53-125">x</span><span class="sxs-lookup"><span data-stu-id="88c53-125">x</span></span>             | <span data-ttu-id="88c53-126">x</span><span class="sxs-lookup"><span data-stu-id="88c53-126">x</span></span>               | <span data-ttu-id="88c53-127">x</span><span class="sxs-lookup"><span data-stu-id="88c53-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="88c53-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="88c53-128">Minimum Shader Model</span></span>

<span data-ttu-id="88c53-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="88c53-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="88c53-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="88c53-130">Shader Model</span></span>                                              | <span data-ttu-id="88c53-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="88c53-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="88c53-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="88c53-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="88c53-133">sì</span><span class="sxs-lookup"><span data-stu-id="88c53-133">yes</span></span>       |
| [<span data-ttu-id="88c53-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="88c53-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="88c53-135">sì</span><span class="sxs-lookup"><span data-stu-id="88c53-135">yes</span></span>       |
| [<span data-ttu-id="88c53-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="88c53-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="88c53-137">sì</span><span class="sxs-lookup"><span data-stu-id="88c53-137">yes</span></span>       |
| [<span data-ttu-id="88c53-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c53-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="88c53-139">no</span><span class="sxs-lookup"><span data-stu-id="88c53-139">no</span></span>        |
| [<span data-ttu-id="88c53-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c53-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="88c53-141">no</span><span class="sxs-lookup"><span data-stu-id="88c53-141">no</span></span>        |
| [<span data-ttu-id="88c53-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c53-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="88c53-143">no</span><span class="sxs-lookup"><span data-stu-id="88c53-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="88c53-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88c53-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c53-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c53-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





