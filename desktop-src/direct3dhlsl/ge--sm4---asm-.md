---
title: GE (SM4-ASM)
description: Confronto a virgola mobile vettoriale a livello di componente maggiore di o uguale a.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398224"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="79401-103">GE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="79401-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="79401-104">Confronto a virgola mobile vettoriale a livello di componente maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="79401-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="79401-105">GE dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="79401-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="79401-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="79401-106">Item</span></span>                                                            | <span data-ttu-id="79401-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79401-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="79401-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="79401-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="79401-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="79401-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="79401-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="79401-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="79401-111">\[nel \] componente da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="79401-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="79401-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="79401-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="79401-113">\[nel \] componente da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="79401-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="79401-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="79401-114">Remarks</span></span>

<span data-ttu-id="79401-115">Esegue il confronto float (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="79401-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="79401-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="79401-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="79401-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="79401-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="79401-118">Le denormazioni vengono scaricate prima del confronto e i registri di origine originali non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="79401-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="79401-119">+ 0 è uguale a-0.</span><span class="sxs-lookup"><span data-stu-id="79401-119">+0 equals -0.</span></span> <span data-ttu-id="79401-120">Il confronto con NaN restituisce false.</span><span class="sxs-lookup"><span data-stu-id="79401-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="79401-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="79401-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="79401-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="79401-122">Vertex Shader</span></span> | <span data-ttu-id="79401-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="79401-123">Geometry Shader</span></span> | <span data-ttu-id="79401-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="79401-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="79401-125">x</span><span class="sxs-lookup"><span data-stu-id="79401-125">x</span></span>             | <span data-ttu-id="79401-126">x</span><span class="sxs-lookup"><span data-stu-id="79401-126">x</span></span>               | <span data-ttu-id="79401-127">x</span><span class="sxs-lookup"><span data-stu-id="79401-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="79401-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="79401-128">Minimum Shader Model</span></span>

<span data-ttu-id="79401-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="79401-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="79401-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="79401-130">Shader Model</span></span>                                              | <span data-ttu-id="79401-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="79401-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="79401-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="79401-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="79401-133">sì</span><span class="sxs-lookup"><span data-stu-id="79401-133">yes</span></span>       |
| [<span data-ttu-id="79401-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="79401-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="79401-135">sì</span><span class="sxs-lookup"><span data-stu-id="79401-135">yes</span></span>       |
| [<span data-ttu-id="79401-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="79401-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="79401-137">sì</span><span class="sxs-lookup"><span data-stu-id="79401-137">yes</span></span>       |
| [<span data-ttu-id="79401-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79401-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="79401-139">no</span><span class="sxs-lookup"><span data-stu-id="79401-139">no</span></span>        |
| [<span data-ttu-id="79401-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79401-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="79401-141">no</span><span class="sxs-lookup"><span data-stu-id="79401-141">no</span></span>        |
| [<span data-ttu-id="79401-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79401-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="79401-143">no</span><span class="sxs-lookup"><span data-stu-id="79401-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="79401-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79401-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79401-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79401-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





