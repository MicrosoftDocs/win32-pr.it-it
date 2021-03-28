---
title: ISHR (SM4-ASM)
description: Spostamento aritmetico a destra (estensione di segno). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995732"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="da5e1-104">ISHR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="da5e1-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="da5e1-105">Spostamento aritmetico a destra (estensione di segno).</span><span class="sxs-lookup"><span data-stu-id="da5e1-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="da5e1-106">ISHR dest \[ . mask \] , src0 \[ . Swizzle \] , src1. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="da5e1-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="da5e1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="da5e1-107">Item</span></span>                                                            | <span data-ttu-id="da5e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da5e1-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="da5e1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="da5e1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="da5e1-110">\[in \] contiene il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="da5e1-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="da5e1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="da5e1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="da5e1-112">\[in \] contiene il valore da spostare.</span><span class="sxs-lookup"><span data-stu-id="da5e1-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="da5e1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="da5e1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="da5e1-114">\[in \] contiene l'importo dello spostamento.</span><span class="sxs-lookup"><span data-stu-id="da5e1-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="da5e1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="da5e1-115">Remarks</span></span>

<span data-ttu-id="da5e1-116">Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) nel *\_ componente src1. Select*, replicando il valore di bit 31.</span><span class="sxs-lookup"><span data-stu-id="da5e1-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="da5e1-117">Il risultato di 32 bit per componente viene inserito in *dest*.</span><span class="sxs-lookup"><span data-stu-id="da5e1-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="da5e1-118">Il conteggio è un valore scalare applicato a tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="da5e1-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="da5e1-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="da5e1-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="da5e1-120">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="da5e1-120">Vertex Shader</span></span> | <span data-ttu-id="da5e1-121">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="da5e1-121">Geometry Shader</span></span> | <span data-ttu-id="da5e1-122">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="da5e1-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="da5e1-123">x</span><span class="sxs-lookup"><span data-stu-id="da5e1-123">x</span></span>             | <span data-ttu-id="da5e1-124">x</span><span class="sxs-lookup"><span data-stu-id="da5e1-124">x</span></span>               | <span data-ttu-id="da5e1-125">x</span><span class="sxs-lookup"><span data-stu-id="da5e1-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da5e1-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="da5e1-126">Minimum Shader Model</span></span>

<span data-ttu-id="da5e1-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="da5e1-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da5e1-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="da5e1-128">Shader Model</span></span>                                              | <span data-ttu-id="da5e1-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="da5e1-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="da5e1-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="da5e1-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="da5e1-131">sì</span><span class="sxs-lookup"><span data-stu-id="da5e1-131">yes</span></span>       |
| [<span data-ttu-id="da5e1-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="da5e1-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="da5e1-133">sì</span><span class="sxs-lookup"><span data-stu-id="da5e1-133">yes</span></span>       |
| [<span data-ttu-id="da5e1-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="da5e1-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="da5e1-135">sì</span><span class="sxs-lookup"><span data-stu-id="da5e1-135">yes</span></span>       |
| [<span data-ttu-id="da5e1-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da5e1-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="da5e1-137">no</span><span class="sxs-lookup"><span data-stu-id="da5e1-137">no</span></span>        |
| [<span data-ttu-id="da5e1-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da5e1-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="da5e1-139">no</span><span class="sxs-lookup"><span data-stu-id="da5e1-139">no</span></span>        |
| [<span data-ttu-id="da5e1-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da5e1-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="da5e1-141">no</span><span class="sxs-lookup"><span data-stu-id="da5e1-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="da5e1-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da5e1-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da5e1-143">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da5e1-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





