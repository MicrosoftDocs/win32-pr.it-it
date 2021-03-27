---
title: deriv_rty_coarse (SM5-ASM)
description: Calcola la frequenza di modifica dei componenti. | deriv_rty_coarse (SM5-ASM)
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995605"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="f3cee-104">derivate \_ valore \_ grossolane (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f3cee-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="f3cee-105">Calcola la frequenza di modifica dei componenti.</span><span class="sxs-lookup"><span data-stu-id="f3cee-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="f3cee-106">derivate \_ valore a \_ grosse \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="f3cee-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="f3cee-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3cee-107">Item</span></span>                                                            | <span data-ttu-id="f3cee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3cee-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f3cee-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f3cee-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f3cee-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f3cee-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f3cee-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f3cee-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f3cee-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f3cee-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f3cee-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3cee-113">Remarks</span></span>

<span data-ttu-id="f3cee-114">Per ulteriori informazioni, vedere [derivare \_ RTX \_ grossolano.](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="f3cee-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="f3cee-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3cee-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f3cee-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="f3cee-116">Vertex</span></span> | <span data-ttu-id="f3cee-117">Hull</span><span class="sxs-lookup"><span data-stu-id="f3cee-117">Hull</span></span> | <span data-ttu-id="f3cee-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="f3cee-118">Domain</span></span> | <span data-ttu-id="f3cee-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="f3cee-119">Geometry</span></span> | <span data-ttu-id="f3cee-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="f3cee-120">Pixel</span></span> | <span data-ttu-id="f3cee-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f3cee-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f3cee-122">X</span><span class="sxs-lookup"><span data-stu-id="f3cee-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f3cee-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f3cee-123">Minimum Shader Model</span></span>

<span data-ttu-id="f3cee-124">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3cee-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f3cee-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f3cee-125">Shader Model</span></span>                                              | <span data-ttu-id="f3cee-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3cee-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f3cee-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f3cee-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f3cee-128">sì</span><span class="sxs-lookup"><span data-stu-id="f3cee-128">yes</span></span>       |
| [<span data-ttu-id="f3cee-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f3cee-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f3cee-130">no</span><span class="sxs-lookup"><span data-stu-id="f3cee-130">no</span></span>        |
| [<span data-ttu-id="f3cee-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f3cee-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f3cee-132">no</span><span class="sxs-lookup"><span data-stu-id="f3cee-132">no</span></span>        |
| [<span data-ttu-id="f3cee-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cee-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f3cee-134">no</span><span class="sxs-lookup"><span data-stu-id="f3cee-134">no</span></span>        |
| [<span data-ttu-id="f3cee-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cee-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f3cee-136">no</span><span class="sxs-lookup"><span data-stu-id="f3cee-136">no</span></span>        |
| [<span data-ttu-id="f3cee-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cee-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f3cee-138">no</span><span class="sxs-lookup"><span data-stu-id="f3cee-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f3cee-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3cee-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3cee-140">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cee-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





