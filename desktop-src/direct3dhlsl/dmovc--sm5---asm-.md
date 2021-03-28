---
title: dmovc (SM5-ASM)
description: Spostamento condizionale a livello di componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401864"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="18678-104">dmovc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="18678-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="18678-105">Spostamento condizionale a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="18678-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="18678-106">dmovc \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="18678-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="18678-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="18678-107">Item</span></span>                                                            | <span data-ttu-id="18678-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18678-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18678-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="18678-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="18678-110">\[nella \] destinazione di spostamento.</span><span class="sxs-lookup"><span data-stu-id="18678-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="18678-111">Se *src0*, quindi *dest*  =  *src1* else *dest*  =  *src2*.</span><span class="sxs-lookup"><span data-stu-id="18678-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="18678-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="18678-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="18678-113">\[nei \] componenti su cui eseguire il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="18678-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="18678-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="18678-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="18678-115">\[nei \] componenti da spostare se la condizione è true.</span><span class="sxs-lookup"><span data-stu-id="18678-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="18678-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="18678-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="18678-117">\[nei \] componenti da spostare se la condizione è false.</span><span class="sxs-lookup"><span data-stu-id="18678-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="18678-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="18678-118">Remarks</span></span>

<span data-ttu-id="18678-119">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="18678-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="18678-120">Le maschere valide per dest sono. XY,. ZW,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="18678-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="18678-121">Il valore di swizzles valido per *src0* è qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="18678-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="18678-122">I primi due componenti post-swizzle vengono usati per identificare i valori di condizione a 2 32 bit.</span><span class="sxs-lookup"><span data-stu-id="18678-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="18678-123">Il valore di swizzles valido per *src1* e *src2* che contiene i valori Double è. xyzw,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="18678-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="18678-124">sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="18678-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="18678-125">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="18678-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="18678-126">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="18678-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="18678-127">*src0* è un vec2 a 32 bit/componente tra x e y (ZW ignorato).</span><span class="sxs-lookup"><span data-stu-id="18678-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="18678-128">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="18678-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="18678-129">*src2* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="18678-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="18678-130">I modificatori in *src1* e *src2*, diversi da Swizzle, presuppongono che i dati siano Double.</span><span class="sxs-lookup"><span data-stu-id="18678-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="18678-131">L'assenza di modificatori sposta i dati senza alterare i bit.</span><span class="sxs-lookup"><span data-stu-id="18678-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="18678-132">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="18678-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="18678-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="18678-133">Vertex</span></span> | <span data-ttu-id="18678-134">Hull</span><span class="sxs-lookup"><span data-stu-id="18678-134">Hull</span></span> | <span data-ttu-id="18678-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="18678-135">Domain</span></span> | <span data-ttu-id="18678-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="18678-136">Geometry</span></span> | <span data-ttu-id="18678-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="18678-137">Pixel</span></span> | <span data-ttu-id="18678-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="18678-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="18678-139">X</span><span class="sxs-lookup"><span data-stu-id="18678-139">X</span></span>      | <span data-ttu-id="18678-140">X</span><span class="sxs-lookup"><span data-stu-id="18678-140">X</span></span>    | <span data-ttu-id="18678-141">X</span><span class="sxs-lookup"><span data-stu-id="18678-141">X</span></span>      | <span data-ttu-id="18678-142">X</span><span class="sxs-lookup"><span data-stu-id="18678-142">X</span></span>        | <span data-ttu-id="18678-143">X</span><span class="sxs-lookup"><span data-stu-id="18678-143">X</span></span>     | <span data-ttu-id="18678-144">X</span><span class="sxs-lookup"><span data-stu-id="18678-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="18678-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="18678-145">Minimum Shader Model</span></span>

<span data-ttu-id="18678-146">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="18678-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="18678-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="18678-147">Shader Model</span></span>                                              | <span data-ttu-id="18678-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="18678-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="18678-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="18678-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="18678-150">sì</span><span class="sxs-lookup"><span data-stu-id="18678-150">yes</span></span>       |
| [<span data-ttu-id="18678-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="18678-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="18678-152">no</span><span class="sxs-lookup"><span data-stu-id="18678-152">no</span></span>        |
| [<span data-ttu-id="18678-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="18678-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="18678-154">no</span><span class="sxs-lookup"><span data-stu-id="18678-154">no</span></span>        |
| [<span data-ttu-id="18678-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18678-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="18678-156">no</span><span class="sxs-lookup"><span data-stu-id="18678-156">no</span></span>        |
| [<span data-ttu-id="18678-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18678-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="18678-158">no</span><span class="sxs-lookup"><span data-stu-id="18678-158">no</span></span>        |
| [<span data-ttu-id="18678-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18678-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="18678-160">no</span><span class="sxs-lookup"><span data-stu-id="18678-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="18678-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18678-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18678-162">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18678-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





