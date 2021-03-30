---
title: RETC (SM4-ASM)
description: Risultato condizionale.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976442"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="3f12d-103">RETC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3f12d-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="3f12d-104">Risultato condizionale.</span><span class="sxs-lookup"><span data-stu-id="3f12d-104">Conditional return.</span></span>



| <span data-ttu-id="3f12d-105">RETC { \_ z </span><span class="sxs-lookup"><span data-stu-id="3f12d-105">retc{\_z</span></span>\|<span data-ttu-id="3f12d-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="3f12d-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="3f12d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3f12d-107">Item</span></span>                                                            | <span data-ttu-id="3f12d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f12d-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3f12d-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3f12d-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3f12d-110">\[nel \] registro in cui verificare la condizione.</span><span class="sxs-lookup"><span data-stu-id="3f12d-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f12d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f12d-111">Remarks</span></span>

<span data-ttu-id="3f12d-112">Se all'interno di una subroutine, questa istruzione restituisce in modo condizionale l'istruzione dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3f12d-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="3f12d-113">Se non si trova all'interno di una subroutine, questa istruzione termina l'esecuzione del programma.</span><span class="sxs-lookup"><span data-stu-id="3f12d-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="3f12d-114">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="3f12d-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="3f12d-115">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="3f12d-115">Restrictions</span></span>

-   <span data-ttu-id="3f12d-116">**RETC** possono essere presenti in qualsiasi punto di un programma, un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="3f12d-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="3f12d-117">L'ultima istruzione in un programma principale o in una subroutine non può essere **RETC \_ z** o **RETC \_ NZ**.</span><span class="sxs-lookup"><span data-stu-id="3f12d-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="3f12d-118">Al contrario, è possibile utilizzare il [ret](ret--sm4---asm-.md) non condizionale.</span><span class="sxs-lookup"><span data-stu-id="3f12d-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="3f12d-119">Il registro a 32 bit fornito da *src0* viene testato a livello di bit.</span><span class="sxs-lookup"><span data-stu-id="3f12d-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="3f12d-120">Se un bit è diverso da zero, **ret \_ NZ** restituirà.</span><span class="sxs-lookup"><span data-stu-id="3f12d-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="3f12d-121">Se tutti i bit sono zero, **RETC \_ z** restituirà.</span><span class="sxs-lookup"><span data-stu-id="3f12d-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="3f12d-122">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3f12d-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3f12d-123">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="3f12d-123">Vertex Shader</span></span> | <span data-ttu-id="3f12d-124">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="3f12d-124">Geometry Shader</span></span> | <span data-ttu-id="3f12d-125">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="3f12d-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3f12d-126">x</span><span class="sxs-lookup"><span data-stu-id="3f12d-126">x</span></span>             | <span data-ttu-id="3f12d-127">x</span><span class="sxs-lookup"><span data-stu-id="3f12d-127">x</span></span>               | <span data-ttu-id="3f12d-128">x</span><span class="sxs-lookup"><span data-stu-id="3f12d-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3f12d-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3f12d-129">Minimum Shader Model</span></span>

<span data-ttu-id="3f12d-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f12d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3f12d-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3f12d-131">Shader Model</span></span>                                              | <span data-ttu-id="3f12d-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="3f12d-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3f12d-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3f12d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3f12d-134">sì</span><span class="sxs-lookup"><span data-stu-id="3f12d-134">yes</span></span>       |
| [<span data-ttu-id="3f12d-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3f12d-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3f12d-136">sì</span><span class="sxs-lookup"><span data-stu-id="3f12d-136">yes</span></span>       |
| [<span data-ttu-id="3f12d-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3f12d-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3f12d-138">sì</span><span class="sxs-lookup"><span data-stu-id="3f12d-138">yes</span></span>       |
| [<span data-ttu-id="3f12d-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f12d-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3f12d-140">no</span><span class="sxs-lookup"><span data-stu-id="3f12d-140">no</span></span>        |
| [<span data-ttu-id="3f12d-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f12d-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3f12d-142">no</span><span class="sxs-lookup"><span data-stu-id="3f12d-142">no</span></span>        |
| [<span data-ttu-id="3f12d-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f12d-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3f12d-144">no</span><span class="sxs-lookup"><span data-stu-id="3f12d-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3f12d-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f12d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f12d-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f12d-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





