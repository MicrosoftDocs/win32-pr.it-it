---
title: o (SM4-ASM)
description: OR bit per bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993152"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="f4660-103">o (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f4660-103">or (sm4 - asm)</span></span>

<span data-ttu-id="f4660-104">OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="f4660-104">Bitwise or.</span></span>



| <span data-ttu-id="f4660-105">o dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f4660-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="f4660-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4660-106">Item</span></span>                                                            | <span data-ttu-id="f4660-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4660-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="f4660-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f4660-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f4660-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f4660-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="f4660-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f4660-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f4660-111">\[nei \] componenti a o con *src1*.</span><span class="sxs-lookup"><span data-stu-id="f4660-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="f4660-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f4660-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f4660-113">\[nei \] componenti a o con *src0*.</span><span class="sxs-lookup"><span data-stu-id="f4660-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4660-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4660-114">Remarks</span></span>

<span data-ttu-id="f4660-115">Questa istruzione esegue un'operazione logica di componente o di ogni coppia di valori a 32 bit da *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="f4660-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="f4660-116">I risultati a 32 bit vengono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="f4660-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="f4660-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4660-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f4660-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="f4660-118">Vertex Shader</span></span> | <span data-ttu-id="f4660-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="f4660-119">Geometry Shader</span></span> | <span data-ttu-id="f4660-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="f4660-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f4660-121">x</span><span class="sxs-lookup"><span data-stu-id="f4660-121">x</span></span>             | <span data-ttu-id="f4660-122">x</span><span class="sxs-lookup"><span data-stu-id="f4660-122">x</span></span>               | <span data-ttu-id="f4660-123">x</span><span class="sxs-lookup"><span data-stu-id="f4660-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f4660-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f4660-124">Minimum Shader Model</span></span>

<span data-ttu-id="f4660-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4660-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f4660-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f4660-126">Shader Model</span></span>                                              | <span data-ttu-id="f4660-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="f4660-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4660-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f4660-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4660-129">sì</span><span class="sxs-lookup"><span data-stu-id="f4660-129">yes</span></span>       |
| [<span data-ttu-id="f4660-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f4660-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4660-131">sì</span><span class="sxs-lookup"><span data-stu-id="f4660-131">yes</span></span>       |
| [<span data-ttu-id="f4660-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f4660-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4660-133">sì</span><span class="sxs-lookup"><span data-stu-id="f4660-133">yes</span></span>       |
| [<span data-ttu-id="f4660-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4660-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4660-135">no</span><span class="sxs-lookup"><span data-stu-id="f4660-135">no</span></span>        |
| [<span data-ttu-id="f4660-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4660-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4660-137">no</span><span class="sxs-lookup"><span data-stu-id="f4660-137">no</span></span>        |
| [<span data-ttu-id="f4660-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4660-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4660-139">no</span><span class="sxs-lookup"><span data-stu-id="f4660-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f4660-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4660-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4660-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4660-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





