---
title: USHR (SM4-ASM)
description: Spostamento a destra. | USHR (SM4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234676"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="a493b-104">USHR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a493b-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="a493b-105">Spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="a493b-105">Shift right.</span></span>



| <span data-ttu-id="a493b-106">USHR dest \[ . mask \] , src0 \[ . Swizzle \] , src1. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="a493b-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="a493b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a493b-107">Item</span></span>                                                            | <span data-ttu-id="a493b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a493b-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a493b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a493b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a493b-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a493b-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="a493b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a493b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a493b-112">\[nei \] componenti da spostare.</span><span class="sxs-lookup"><span data-stu-id="a493b-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="a493b-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a493b-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a493b-114">\[nel \] valore da spostare *src0*.</span><span class="sxs-lookup"><span data-stu-id="a493b-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="a493b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a493b-115">Remarks</span></span>

<span data-ttu-id="a493b-116">Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1. Select \_ componente*, inserendo 0.</span><span class="sxs-lookup"><span data-stu-id="a493b-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="a493b-117">Il risultato di 32 bit per componente viene inserito in *dest*.</span><span class="sxs-lookup"><span data-stu-id="a493b-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="a493b-118">Il conteggio è un valore scalare applicato a tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="a493b-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="a493b-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a493b-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a493b-120">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a493b-120">Vertex Shader</span></span> | <span data-ttu-id="a493b-121">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a493b-121">Geometry Shader</span></span> | <span data-ttu-id="a493b-122">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a493b-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a493b-123">x</span><span class="sxs-lookup"><span data-stu-id="a493b-123">x</span></span>             | <span data-ttu-id="a493b-124">x</span><span class="sxs-lookup"><span data-stu-id="a493b-124">x</span></span>               | <span data-ttu-id="a493b-125">x</span><span class="sxs-lookup"><span data-stu-id="a493b-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a493b-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a493b-126">Minimum Shader Model</span></span>

<span data-ttu-id="a493b-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a493b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a493b-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a493b-128">Shader Model</span></span>                                              | <span data-ttu-id="a493b-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="a493b-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a493b-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a493b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a493b-131">sì</span><span class="sxs-lookup"><span data-stu-id="a493b-131">yes</span></span>       |
| [<span data-ttu-id="a493b-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a493b-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a493b-133">sì</span><span class="sxs-lookup"><span data-stu-id="a493b-133">yes</span></span>       |
| [<span data-ttu-id="a493b-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a493b-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a493b-135">sì</span><span class="sxs-lookup"><span data-stu-id="a493b-135">yes</span></span>       |
| [<span data-ttu-id="a493b-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a493b-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a493b-137">no</span><span class="sxs-lookup"><span data-stu-id="a493b-137">no</span></span>        |
| [<span data-ttu-id="a493b-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a493b-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a493b-139">no</span><span class="sxs-lookup"><span data-stu-id="a493b-139">no</span></span>        |
| [<span data-ttu-id="a493b-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a493b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a493b-141">no</span><span class="sxs-lookup"><span data-stu-id="a493b-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a493b-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a493b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a493b-143">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a493b-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





