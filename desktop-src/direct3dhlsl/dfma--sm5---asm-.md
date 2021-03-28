---
title: DFMA (SM5-ASM)
description: Esegue un'aggiunta di moltiplicazione con fusione.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335503"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="acffb-103">DFMA (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="acffb-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="acffb-104">Esegue un'aggiunta di moltiplicazione con fusione.</span><span class="sxs-lookup"><span data-stu-id="acffb-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="acffb-105">DFMA \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="acffb-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="acffb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="acffb-106">Item</span></span>                                                            | <span data-ttu-id="acffb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acffb-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acffb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="acffb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="acffb-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="acffb-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="acffb-110">Il valore del risultato deve essere accurato per 0,5 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="acffb-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="acffb-111">*dest*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="acffb-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="acffb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="acffb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="acffb-113">\[nei \] componenti da moltiplicare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="acffb-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="acffb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="acffb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="acffb-115">\[nei \] componenti da moltiplicare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="acffb-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="acffb-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="acffb-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="acffb-117">\[nei \] componenti da aggiungere a *src0* \* *src1*.</span><span class="sxs-lookup"><span data-stu-id="acffb-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="acffb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="acffb-118">Remarks</span></span>

<span data-ttu-id="acffb-119">Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà la mancata associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="acffb-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="acffb-120">Il sistema supporta DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="acffb-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="acffb-121">Il sistema include un driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="acffb-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="acffb-122">Il driver segnala il supporto per questa istruzione tramite le **\_ \_ Opzioni d3d11 dei dati della funzionalità d3d11 \_ \_ . ExtendedDoublesShaderInstructions** impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="acffb-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="acffb-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="acffb-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="acffb-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="acffb-124">Vertex</span></span> | <span data-ttu-id="acffb-125">Hull</span><span class="sxs-lookup"><span data-stu-id="acffb-125">Hull</span></span> | <span data-ttu-id="acffb-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="acffb-126">Domain</span></span> | <span data-ttu-id="acffb-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="acffb-127">Geometry</span></span> | <span data-ttu-id="acffb-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="acffb-128">Pixel</span></span> | <span data-ttu-id="acffb-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="acffb-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="acffb-130">X</span><span class="sxs-lookup"><span data-stu-id="acffb-130">X</span></span>      | <span data-ttu-id="acffb-131">X</span><span class="sxs-lookup"><span data-stu-id="acffb-131">X</span></span>    | <span data-ttu-id="acffb-132">X</span><span class="sxs-lookup"><span data-stu-id="acffb-132">X</span></span>      | <span data-ttu-id="acffb-133">X</span><span class="sxs-lookup"><span data-stu-id="acffb-133">X</span></span>        | <span data-ttu-id="acffb-134">X</span><span class="sxs-lookup"><span data-stu-id="acffb-134">X</span></span>     | <span data-ttu-id="acffb-135">X</span><span class="sxs-lookup"><span data-stu-id="acffb-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="acffb-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="acffb-136">Minimum Shader Model</span></span>

<span data-ttu-id="acffb-137">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="acffb-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="acffb-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="acffb-138">Shader Model</span></span>                                              | <span data-ttu-id="acffb-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="acffb-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="acffb-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="acffb-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="acffb-141">sì</span><span class="sxs-lookup"><span data-stu-id="acffb-141">yes</span></span>       |
| [<span data-ttu-id="acffb-142">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="acffb-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="acffb-143">no</span><span class="sxs-lookup"><span data-stu-id="acffb-143">no</span></span>        |
| [<span data-ttu-id="acffb-144">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="acffb-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="acffb-145">no</span><span class="sxs-lookup"><span data-stu-id="acffb-145">no</span></span>        |
| [<span data-ttu-id="acffb-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acffb-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="acffb-147">no</span><span class="sxs-lookup"><span data-stu-id="acffb-147">no</span></span>        |
| [<span data-ttu-id="acffb-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acffb-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="acffb-149">no</span><span class="sxs-lookup"><span data-stu-id="acffb-149">no</span></span>        |
| [<span data-ttu-id="acffb-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acffb-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="acffb-151">no</span><span class="sxs-lookup"><span data-stu-id="acffb-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="acffb-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acffb-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acffb-153">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acffb-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





