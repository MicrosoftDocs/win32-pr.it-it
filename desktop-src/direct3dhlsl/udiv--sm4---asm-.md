---
title: udiv (SM4-ASM)
description: Divisione di interi senza segno.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398240"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="4a6c2-103">udiv (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4a6c2-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="4a6c2-104">Divisione di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="4a6c2-105">udiv destQUOT \[ . mask \] , destREM \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4a6c2-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="4a6c2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a6c2-106">Item</span></span>                                                                                                   | <span data-ttu-id="4a6c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a6c2-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4a6c2-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span><span class="sxs-lookup"><span data-stu-id="4a6c2-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="4a6c2-109">\[nell' \] indirizzo del quoziente risultante.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="4a6c2-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span><span class="sxs-lookup"><span data-stu-id="4a6c2-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="4a6c2-111">\[nell' \] indirizzo del resto risultante.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="4a6c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4a6c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="4a6c2-113">\[nei \] componenti da dividere per *src1*.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="4a6c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4a6c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="4a6c2-115">\[nei \] componenti di serve per dividere *src0*.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a6c2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a6c2-116">Remarks</span></span>

<span data-ttu-id="4a6c2-117">Questa istruzione esegue una divisione senza segno a livello di componente dell'operando a 32 bit *src0* dall'operando *src1* a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="4a6c2-118">I risultati delle divisioni sono i quozienti a 32 bit posizionati in *destQUOT* e i restanti 32 bit posizionati in *destREM*.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="4a6c2-119">Divide per zero restituisce 0xFFFFFFFF per quoziente e resto.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="4a6c2-120">È possibile specificare *destQUOT* o *destREM* come null anziché specificare un registro, se il quoziente o il resto non sono necessari.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="4a6c2-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a6c2-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4a6c2-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="4a6c2-122">Vertex Shader</span></span> | <span data-ttu-id="4a6c2-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="4a6c2-123">Geometry Shader</span></span> | <span data-ttu-id="4a6c2-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="4a6c2-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4a6c2-125">x</span><span class="sxs-lookup"><span data-stu-id="4a6c2-125">x</span></span>             | <span data-ttu-id="4a6c2-126">x</span><span class="sxs-lookup"><span data-stu-id="4a6c2-126">x</span></span>               | <span data-ttu-id="4a6c2-127">x</span><span class="sxs-lookup"><span data-stu-id="4a6c2-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a6c2-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4a6c2-128">Minimum Shader Model</span></span>

<span data-ttu-id="4a6c2-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4a6c2-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4a6c2-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4a6c2-130">Shader Model</span></span>                                              | <span data-ttu-id="4a6c2-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="4a6c2-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4a6c2-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4a6c2-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4a6c2-133">sì</span><span class="sxs-lookup"><span data-stu-id="4a6c2-133">yes</span></span>       |
| [<span data-ttu-id="4a6c2-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="4a6c2-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4a6c2-135">sì</span><span class="sxs-lookup"><span data-stu-id="4a6c2-135">yes</span></span>       |
| [<span data-ttu-id="4a6c2-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="4a6c2-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4a6c2-137">sì</span><span class="sxs-lookup"><span data-stu-id="4a6c2-137">yes</span></span>       |
| [<span data-ttu-id="4a6c2-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a6c2-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4a6c2-139">no</span><span class="sxs-lookup"><span data-stu-id="4a6c2-139">no</span></span>        |
| [<span data-ttu-id="4a6c2-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a6c2-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4a6c2-141">no</span><span class="sxs-lookup"><span data-stu-id="4a6c2-141">no</span></span>        |
| [<span data-ttu-id="4a6c2-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a6c2-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4a6c2-143">no</span><span class="sxs-lookup"><span data-stu-id="4a6c2-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4a6c2-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a6c2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a6c2-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a6c2-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





