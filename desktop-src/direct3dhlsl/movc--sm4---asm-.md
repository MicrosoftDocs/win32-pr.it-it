---
title: MOVC (SM4-ASM)
description: Spostamento condizionale a livello di componente. | MOVC (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995477"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="0fce9-104">MOVC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0fce9-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="0fce9-105">Spostamento condizionale a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="0fce9-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="0fce9-106">MOVC \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="0fce9-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0fce9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fce9-107">Item</span></span>                                                            | <span data-ttu-id="0fce9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fce9-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fce9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0fce9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0fce9-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0fce9-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="0fce9-111">Se *src0*, quindi *dest*  =  *src1* else *dest*  =  *src2*</span><span class="sxs-lookup"><span data-stu-id="0fce9-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="0fce9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0fce9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0fce9-113">\[nei \] componenti su cui eseguire il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="0fce9-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="0fce9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0fce9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0fce9-115">\[nei \] componenti da spostare.</span><span class="sxs-lookup"><span data-stu-id="0fce9-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="0fce9-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="0fce9-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="0fce9-117">\[nei \] componenti da spostare.</span><span class="sxs-lookup"><span data-stu-id="0fce9-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0fce9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fce9-118">Remarks</span></span>

<span data-ttu-id="0fce9-119">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="0fce9-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="0fce9-120">I modificatori in *src1* e *src2*, diversi da Swizzle, presuppongono che i dati siano a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="0fce9-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="0fce9-121">L'assenza di modificatori sposta solo i dati senza alterare i bit.</span><span class="sxs-lookup"><span data-stu-id="0fce9-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="0fce9-122">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fce9-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0fce9-123">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0fce9-123">Vertex Shader</span></span> | <span data-ttu-id="0fce9-124">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="0fce9-124">Geometry Shader</span></span> | <span data-ttu-id="0fce9-125">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="0fce9-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0fce9-126">x</span><span class="sxs-lookup"><span data-stu-id="0fce9-126">x</span></span>             | <span data-ttu-id="0fce9-127">x</span><span class="sxs-lookup"><span data-stu-id="0fce9-127">x</span></span>               | <span data-ttu-id="0fce9-128">x</span><span class="sxs-lookup"><span data-stu-id="0fce9-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0fce9-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0fce9-129">Minimum Shader Model</span></span>

<span data-ttu-id="0fce9-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0fce9-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0fce9-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0fce9-131">Shader Model</span></span>                                              | <span data-ttu-id="0fce9-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="0fce9-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0fce9-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0fce9-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0fce9-134">sì</span><span class="sxs-lookup"><span data-stu-id="0fce9-134">yes</span></span>       |
| [<span data-ttu-id="0fce9-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="0fce9-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0fce9-136">sì</span><span class="sxs-lookup"><span data-stu-id="0fce9-136">yes</span></span>       |
| [<span data-ttu-id="0fce9-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0fce9-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0fce9-138">sì</span><span class="sxs-lookup"><span data-stu-id="0fce9-138">yes</span></span>       |
| [<span data-ttu-id="0fce9-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fce9-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0fce9-140">no</span><span class="sxs-lookup"><span data-stu-id="0fce9-140">no</span></span>        |
| [<span data-ttu-id="0fce9-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fce9-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0fce9-142">no</span><span class="sxs-lookup"><span data-stu-id="0fce9-142">no</span></span>        |
| [<span data-ttu-id="0fce9-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fce9-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0fce9-144">no</span><span class="sxs-lookup"><span data-stu-id="0fce9-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0fce9-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fce9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fce9-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fce9-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





