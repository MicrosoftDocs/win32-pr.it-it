---
title: IAdd (SM4-ASM)
description: Aggiunta Integer.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398278"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="086a3-103">IAdd (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="086a3-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="086a3-104">Aggiunta Integer.</span><span class="sxs-lookup"><span data-stu-id="086a3-104">Integer addition.</span></span>



| <span data-ttu-id="086a3-105">IAdd dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="086a3-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="086a3-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="086a3-106">Item</span></span>                                                            | <span data-ttu-id="086a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="086a3-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="086a3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="086a3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="086a3-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="086a3-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="086a3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="086a3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="086a3-111">\[nel \] numero da aggiungere a *src1*.</span><span class="sxs-lookup"><span data-stu-id="086a3-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="086a3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="086a3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="086a3-113">\[nel \] numero da aggiungere a *src0*.</span><span class="sxs-lookup"><span data-stu-id="086a3-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="086a3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="086a3-114">Remarks</span></span>

<span data-ttu-id="086a3-115">Aggiunta a livello di componente di operandi a 32 bit *src0* e *src1*, inserendo il risultato corretto a 32 bit in *dest*.</span><span class="sxs-lookup"><span data-stu-id="086a3-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="086a3-116">Non viene eseguita alcuna operazione Carry o borrow oltre i valori a 32 bit di ogni componente, quindi questa istruzione non è sensibile alla firma degli operandi.</span><span class="sxs-lookup"><span data-stu-id="086a3-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="086a3-117">Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="086a3-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="086a3-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="086a3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="086a3-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="086a3-119">Vertex Shader</span></span> | <span data-ttu-id="086a3-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="086a3-120">Geometry Shader</span></span> | <span data-ttu-id="086a3-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="086a3-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="086a3-122">x</span><span class="sxs-lookup"><span data-stu-id="086a3-122">x</span></span>             | <span data-ttu-id="086a3-123">x</span><span class="sxs-lookup"><span data-stu-id="086a3-123">x</span></span>               | <span data-ttu-id="086a3-124">x</span><span class="sxs-lookup"><span data-stu-id="086a3-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="086a3-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="086a3-125">Minimum Shader Model</span></span>

<span data-ttu-id="086a3-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="086a3-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="086a3-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="086a3-127">Shader Model</span></span>                                              | <span data-ttu-id="086a3-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="086a3-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="086a3-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="086a3-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="086a3-130">sì</span><span class="sxs-lookup"><span data-stu-id="086a3-130">yes</span></span>       |
| [<span data-ttu-id="086a3-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="086a3-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="086a3-132">sì</span><span class="sxs-lookup"><span data-stu-id="086a3-132">yes</span></span>       |
| [<span data-ttu-id="086a3-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="086a3-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="086a3-134">sì</span><span class="sxs-lookup"><span data-stu-id="086a3-134">yes</span></span>       |
| [<span data-ttu-id="086a3-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="086a3-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="086a3-136">no</span><span class="sxs-lookup"><span data-stu-id="086a3-136">no</span></span>        |
| [<span data-ttu-id="086a3-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="086a3-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="086a3-138">no</span><span class="sxs-lookup"><span data-stu-id="086a3-138">no</span></span>        |
| [<span data-ttu-id="086a3-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="086a3-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="086a3-140">no</span><span class="sxs-lookup"><span data-stu-id="086a3-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="086a3-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="086a3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="086a3-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="086a3-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





