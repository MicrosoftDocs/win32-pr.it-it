---
title: ineg (SM4-ASM)
description: complemento 2.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398268"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="bace4-103">ineg (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bace4-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="bace4-104">complemento 2.</span><span class="sxs-lookup"><span data-stu-id="bace4-104">2's complement.</span></span>



| <span data-ttu-id="bace4-105">ineg dest \[ . mask \] , src0 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="bace4-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="bace4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="bace4-106">Item</span></span>                                                            | <span data-ttu-id="bace4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bace4-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bace4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bace4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bace4-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bace4-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="bace4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bace4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bace4-111">\[in \] contiene i valori per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bace4-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="bace4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bace4-112">Remarks</span></span>

<span data-ttu-id="bace4-113">Questa istruzione esegue il complemento Component-Wise 2 di ogni valore a 32 bit in *src0*.</span><span class="sxs-lookup"><span data-stu-id="bace4-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="bace4-114">I risultati a 32 bit vengono archiviati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="bace4-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="bace4-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bace4-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bace4-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="bace4-116">Vertex Shader</span></span> | <span data-ttu-id="bace4-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="bace4-117">Geometry Shader</span></span> | <span data-ttu-id="bace4-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="bace4-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bace4-119">x</span><span class="sxs-lookup"><span data-stu-id="bace4-119">x</span></span>             | <span data-ttu-id="bace4-120">x</span><span class="sxs-lookup"><span data-stu-id="bace4-120">x</span></span>               | <span data-ttu-id="bace4-121">x</span><span class="sxs-lookup"><span data-stu-id="bace4-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bace4-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bace4-122">Minimum Shader Model</span></span>

<span data-ttu-id="bace4-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bace4-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bace4-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bace4-124">Shader Model</span></span>                                              | <span data-ttu-id="bace4-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="bace4-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bace4-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bace4-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bace4-127">sì</span><span class="sxs-lookup"><span data-stu-id="bace4-127">yes</span></span>       |
| [<span data-ttu-id="bace4-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="bace4-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bace4-129">sì</span><span class="sxs-lookup"><span data-stu-id="bace4-129">yes</span></span>       |
| [<span data-ttu-id="bace4-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="bace4-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bace4-131">sì</span><span class="sxs-lookup"><span data-stu-id="bace4-131">yes</span></span>       |
| [<span data-ttu-id="bace4-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bace4-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bace4-133">no</span><span class="sxs-lookup"><span data-stu-id="bace4-133">no</span></span>        |
| [<span data-ttu-id="bace4-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bace4-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bace4-135">no</span><span class="sxs-lookup"><span data-stu-id="bace4-135">no</span></span>        |
| [<span data-ttu-id="bace4-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bace4-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bace4-137">no</span><span class="sxs-lookup"><span data-stu-id="bace4-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bace4-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bace4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bace4-139">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bace4-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





