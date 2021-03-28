---
title: ISHR (SM5-ASM)
description: Spostamento aritmetico a destra (estensione di segno). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995729"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="f5c02-104">ISHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f5c02-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="f5c02-105">Spostamento aritmetico a destra (estensione di segno).</span><span class="sxs-lookup"><span data-stu-id="f5c02-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="f5c02-106">ISHL dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f5c02-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="f5c02-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5c02-107">Item</span></span>                                                            | <span data-ttu-id="f5c02-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5c02-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5c02-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f5c02-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f5c02-110">\[in \] contiene i risultati dello spostamento.</span><span class="sxs-lookup"><span data-stu-id="f5c02-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="f5c02-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f5c02-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f5c02-112">\[\]numero di bit da spostare.</span><span class="sxs-lookup"><span data-stu-id="f5c02-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="f5c02-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f5c02-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f5c02-114">\[nei \] valori a 32 bit da spostare.</span><span class="sxs-lookup"><span data-stu-id="f5c02-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="f5c02-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5c02-115">Remarks</span></span>

<span data-ttu-id="f5c02-116">Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1*, replicando il valore di bit 31.</span><span class="sxs-lookup"><span data-stu-id="f5c02-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="f5c02-117">Il risultato di 32 bit per componente viene inserito in *dest*.</span><span class="sxs-lookup"><span data-stu-id="f5c02-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="f5c02-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5c02-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f5c02-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="f5c02-119">Vertex</span></span> | <span data-ttu-id="f5c02-120">Hull</span><span class="sxs-lookup"><span data-stu-id="f5c02-120">Hull</span></span> | <span data-ttu-id="f5c02-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="f5c02-121">Domain</span></span> | <span data-ttu-id="f5c02-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="f5c02-122">Geometry</span></span> | <span data-ttu-id="f5c02-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="f5c02-123">Pixel</span></span> | <span data-ttu-id="f5c02-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f5c02-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f5c02-125">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-125">X</span></span>      | <span data-ttu-id="f5c02-126">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-126">X</span></span>    | <span data-ttu-id="f5c02-127">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-127">X</span></span>      | <span data-ttu-id="f5c02-128">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-128">X</span></span>        | <span data-ttu-id="f5c02-129">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-129">X</span></span>     | <span data-ttu-id="f5c02-130">X</span><span class="sxs-lookup"><span data-stu-id="f5c02-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f5c02-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f5c02-131">Minimum Shader Model</span></span>

<span data-ttu-id="f5c02-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5c02-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f5c02-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f5c02-133">Shader Model</span></span>                                              | <span data-ttu-id="f5c02-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="f5c02-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f5c02-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f5c02-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f5c02-136">sì</span><span class="sxs-lookup"><span data-stu-id="f5c02-136">yes</span></span>       |
| [<span data-ttu-id="f5c02-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f5c02-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f5c02-138">no</span><span class="sxs-lookup"><span data-stu-id="f5c02-138">no</span></span>        |
| [<span data-ttu-id="f5c02-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f5c02-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f5c02-140">no</span><span class="sxs-lookup"><span data-stu-id="f5c02-140">no</span></span>        |
| [<span data-ttu-id="f5c02-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c02-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f5c02-142">no</span><span class="sxs-lookup"><span data-stu-id="f5c02-142">no</span></span>        |
| [<span data-ttu-id="f5c02-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c02-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f5c02-144">no</span><span class="sxs-lookup"><span data-stu-id="f5c02-144">no</span></span>        |
| [<span data-ttu-id="f5c02-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c02-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f5c02-146">no</span><span class="sxs-lookup"><span data-stu-id="f5c02-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f5c02-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5c02-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c02-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c02-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





