---
title: MAD (SM4-ASM)
description: Aggiunta di moltiplicazione componente.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046073"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="637aa-103">MAD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="637aa-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="637aa-104">Moltiplicazione componente & aggiunta.</span><span class="sxs-lookup"><span data-stu-id="637aa-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="637aa-105">: MAD \[ \_ Sab \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="637aa-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="637aa-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="637aa-106">Item</span></span>                                                            | <span data-ttu-id="637aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="637aa-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="637aa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="637aa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="637aa-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="637aa-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="637aa-110">*dest*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="637aa-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="637aa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="637aa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="637aa-112">\[in \] multiplicand.</span><span class="sxs-lookup"><span data-stu-id="637aa-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="637aa-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="637aa-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="637aa-114">\[nel \] moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="637aa-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="637aa-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="637aa-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="637aa-116">\[in \] Addend.</span><span class="sxs-lookup"><span data-stu-id="637aa-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="637aa-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="637aa-117">Remarks</span></span>

<span data-ttu-id="637aa-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="637aa-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="637aa-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="637aa-119">Vertex Shader</span></span> | <span data-ttu-id="637aa-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="637aa-120">Geometry Shader</span></span> | <span data-ttu-id="637aa-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="637aa-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="637aa-122">x</span><span class="sxs-lookup"><span data-stu-id="637aa-122">x</span></span>             | <span data-ttu-id="637aa-123">x</span><span class="sxs-lookup"><span data-stu-id="637aa-123">x</span></span>               | <span data-ttu-id="637aa-124">x</span><span class="sxs-lookup"><span data-stu-id="637aa-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="637aa-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="637aa-125">Minimum Shader Model</span></span>

<span data-ttu-id="637aa-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="637aa-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="637aa-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="637aa-127">Shader Model</span></span>                                              | <span data-ttu-id="637aa-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="637aa-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="637aa-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="637aa-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="637aa-130">sì</span><span class="sxs-lookup"><span data-stu-id="637aa-130">yes</span></span>       |
| [<span data-ttu-id="637aa-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="637aa-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="637aa-132">sì</span><span class="sxs-lookup"><span data-stu-id="637aa-132">yes</span></span>       |
| [<span data-ttu-id="637aa-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="637aa-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="637aa-134">sì</span><span class="sxs-lookup"><span data-stu-id="637aa-134">yes</span></span>       |
| [<span data-ttu-id="637aa-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="637aa-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="637aa-136">no</span><span class="sxs-lookup"><span data-stu-id="637aa-136">no</span></span>        |
| [<span data-ttu-id="637aa-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="637aa-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="637aa-138">no</span><span class="sxs-lookup"><span data-stu-id="637aa-138">no</span></span>        |
| [<span data-ttu-id="637aa-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="637aa-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="637aa-140">no</span><span class="sxs-lookup"><span data-stu-id="637aa-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="637aa-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="637aa-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="637aa-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="637aa-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





