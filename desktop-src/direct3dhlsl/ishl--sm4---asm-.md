---
title: ISHL (SM4-ASM)
description: Spostamento a sinistra. | ISHL (SM4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995581"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="2b576-104">ISHL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2b576-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="2b576-105">Spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2b576-105">Shift left.</span></span>



| <span data-ttu-id="2b576-106">dest \[ . mask \] , src0 \[ . Swizzle \] , src1. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="2b576-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="2b576-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b576-107">Item</span></span>                                                            | <span data-ttu-id="2b576-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b576-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2b576-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2b576-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2b576-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2b576-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="2b576-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2b576-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2b576-112">\[in \] contiene i valori da spostare.</span><span class="sxs-lookup"><span data-stu-id="2b576-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="2b576-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2b576-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2b576-114">\[in \] contiene l'importo dello spostamento.</span><span class="sxs-lookup"><span data-stu-id="2b576-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2b576-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b576-115">Remarks</span></span>

<span data-ttu-id="2b576-116">Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a sinistra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1. Select \_ componente*, inserendo 0.</span><span class="sxs-lookup"><span data-stu-id="2b576-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="2b576-117">I risultati a 32 bit per componente sono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="2b576-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="2b576-118">Il conteggio è un valore scalare applicato a tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="2b576-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="2b576-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b576-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2b576-120">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2b576-120">Vertex Shader</span></span> | <span data-ttu-id="2b576-121">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2b576-121">Geometry Shader</span></span> | <span data-ttu-id="2b576-122">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2b576-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2b576-123">x</span><span class="sxs-lookup"><span data-stu-id="2b576-123">x</span></span>             | <span data-ttu-id="2b576-124">x</span><span class="sxs-lookup"><span data-stu-id="2b576-124">x</span></span>               | <span data-ttu-id="2b576-125">x</span><span class="sxs-lookup"><span data-stu-id="2b576-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2b576-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2b576-126">Minimum Shader Model</span></span>

<span data-ttu-id="2b576-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b576-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b576-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2b576-128">Shader Model</span></span>                                              | <span data-ttu-id="2b576-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="2b576-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2b576-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2b576-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2b576-131">sì</span><span class="sxs-lookup"><span data-stu-id="2b576-131">yes</span></span>       |
| [<span data-ttu-id="2b576-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2b576-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2b576-133">sì</span><span class="sxs-lookup"><span data-stu-id="2b576-133">yes</span></span>       |
| [<span data-ttu-id="2b576-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2b576-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2b576-135">sì</span><span class="sxs-lookup"><span data-stu-id="2b576-135">yes</span></span>       |
| [<span data-ttu-id="2b576-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b576-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2b576-137">no</span><span class="sxs-lookup"><span data-stu-id="2b576-137">no</span></span>        |
| [<span data-ttu-id="2b576-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b576-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2b576-139">no</span><span class="sxs-lookup"><span data-stu-id="2b576-139">no</span></span>        |
| [<span data-ttu-id="2b576-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b576-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2b576-141">no</span><span class="sxs-lookup"><span data-stu-id="2b576-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b576-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b576-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b576-143">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b576-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





