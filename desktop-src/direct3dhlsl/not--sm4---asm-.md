---
title: Not (SM4-ASM)
description: NOT bit per bit.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976450"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="ffb6d-103">Not (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ffb6d-103">not (sm4 - asm)</span></span>

<span data-ttu-id="ffb6d-104">NOT bit per bit.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-104">Bitwise not.</span></span>



| <span data-ttu-id="ffb6d-105">not dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ffb6d-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="ffb6d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffb6d-106">Item</span></span>                                                            | <span data-ttu-id="ffb6d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffb6d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ffb6d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ffb6d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ffb6d-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="ffb6d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ffb6d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ffb6d-111">\[nei \] componenti originali.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ffb6d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffb6d-112">Remarks</span></span>

<span data-ttu-id="ffb6d-113">Questa istruzione esegue un complemento di un componente per ogni valore a 32 bit in *src0*.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="ffb6d-114">I risultati a 32 bit vengono archiviati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="ffb6d-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffb6d-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ffb6d-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="ffb6d-116">Vertex Shader</span></span> | <span data-ttu-id="ffb6d-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="ffb6d-117">Geometry Shader</span></span> | <span data-ttu-id="ffb6d-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="ffb6d-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ffb6d-119">x</span><span class="sxs-lookup"><span data-stu-id="ffb6d-119">x</span></span>             | <span data-ttu-id="ffb6d-120">x</span><span class="sxs-lookup"><span data-stu-id="ffb6d-120">x</span></span>               | <span data-ttu-id="ffb6d-121">x</span><span class="sxs-lookup"><span data-stu-id="ffb6d-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ffb6d-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ffb6d-122">Minimum Shader Model</span></span>

<span data-ttu-id="ffb6d-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ffb6d-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ffb6d-124">Shader Model</span></span>                                              | <span data-ttu-id="ffb6d-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="ffb6d-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ffb6d-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ffb6d-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ffb6d-127">sì</span><span class="sxs-lookup"><span data-stu-id="ffb6d-127">yes</span></span>       |
| [<span data-ttu-id="ffb6d-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ffb6d-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ffb6d-129">sì</span><span class="sxs-lookup"><span data-stu-id="ffb6d-129">yes</span></span>       |
| [<span data-ttu-id="ffb6d-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ffb6d-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ffb6d-131">sì</span><span class="sxs-lookup"><span data-stu-id="ffb6d-131">yes</span></span>       |
| [<span data-ttu-id="ffb6d-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffb6d-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ffb6d-133">no</span><span class="sxs-lookup"><span data-stu-id="ffb6d-133">no</span></span>        |
| [<span data-ttu-id="ffb6d-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffb6d-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ffb6d-135">no</span><span class="sxs-lookup"><span data-stu-id="ffb6d-135">no</span></span>        |
| [<span data-ttu-id="ffb6d-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffb6d-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ffb6d-137">no</span><span class="sxs-lookup"><span data-stu-id="ffb6d-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ffb6d-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ffb6d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffb6d-139">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffb6d-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





