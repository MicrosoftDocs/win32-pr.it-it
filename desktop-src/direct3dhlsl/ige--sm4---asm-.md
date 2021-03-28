---
title: IgE (SM4-ASM)
description: Confronto di tipo Integer di un vettore a livello di componente maggiore di o uguale a.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117188"
---
# <a name="ige-sm4---asm"></a><span data-ttu-id="564e4-103">IgE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="564e4-103">ige (sm4 - asm)</span></span>

<span data-ttu-id="564e4-104">Confronto di tipo Integer di un vettore a livello di componente maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="564e4-104">Component-wise vector integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="564e4-105">destinazione IgE \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="564e4-105">ige dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="564e4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="564e4-106">Item</span></span>                                                            | <span data-ttu-id="564e4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="564e4-107">Description</span></span>                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="564e4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="564e4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="564e4-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="564e4-109">\[in\] The result of the operation.</span></span><br/>        |
| <span data-ttu-id="564e4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="564e4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="564e4-111">\[nel \] componente da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="564e4-111">\[in\] The component to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="564e4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="564e4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="564e4-113">\[nel \] componente da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="564e4-113">\[in\] The component to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="564e4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="564e4-114">Remarks</span></span>

<span data-ttu-id="564e4-115">Esegue il confronto di interi (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="564e4-115">Performs the integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="564e4-116">Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente.</span><span class="sxs-lookup"><span data-stu-id="564e4-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="564e4-117">In caso contrario, viene restituito 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="564e4-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="564e4-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="564e4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="564e4-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="564e4-119">Vertex Shader</span></span> | <span data-ttu-id="564e4-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="564e4-120">Geometry Shader</span></span> | <span data-ttu-id="564e4-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="564e4-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="564e4-122">x</span><span class="sxs-lookup"><span data-stu-id="564e4-122">x</span></span>             | <span data-ttu-id="564e4-123">x</span><span class="sxs-lookup"><span data-stu-id="564e4-123">x</span></span>               | <span data-ttu-id="564e4-124">x</span><span class="sxs-lookup"><span data-stu-id="564e4-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="564e4-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="564e4-125">Minimum Shader Model</span></span>

<span data-ttu-id="564e4-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="564e4-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="564e4-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="564e4-127">Shader Model</span></span>                                              | <span data-ttu-id="564e4-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="564e4-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="564e4-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="564e4-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="564e4-130">sì</span><span class="sxs-lookup"><span data-stu-id="564e4-130">yes</span></span>       |
| [<span data-ttu-id="564e4-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="564e4-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="564e4-132">sì</span><span class="sxs-lookup"><span data-stu-id="564e4-132">yes</span></span>       |
| [<span data-ttu-id="564e4-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="564e4-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="564e4-134">sì</span><span class="sxs-lookup"><span data-stu-id="564e4-134">yes</span></span>       |
| [<span data-ttu-id="564e4-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="564e4-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="564e4-136">no</span><span class="sxs-lookup"><span data-stu-id="564e4-136">no</span></span>        |
| [<span data-ttu-id="564e4-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="564e4-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="564e4-138">no</span><span class="sxs-lookup"><span data-stu-id="564e4-138">no</span></span>        |
| [<span data-ttu-id="564e4-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="564e4-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="564e4-140">no</span><span class="sxs-lookup"><span data-stu-id="564e4-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="564e4-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="564e4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564e4-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="564e4-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





