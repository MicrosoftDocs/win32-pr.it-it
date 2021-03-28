---
title: if (SM4-ASM)
description: Ramo basato sul risultato logico o.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992965"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="d0135-103">if (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d0135-103">if (sm4 - asm)</span></span>

<span data-ttu-id="d0135-104">Ramo basato sul risultato logico o.</span><span class="sxs-lookup"><span data-stu-id="d0135-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="d0135-105">Se { \_ z </span><span class="sxs-lookup"><span data-stu-id="d0135-105">if{\_z</span></span>\|<span data-ttu-id="d0135-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="d0135-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="d0135-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d0135-107">Item</span></span>                                                            | <span data-ttu-id="d0135-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0135-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d0135-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d0135-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d0135-110">\[in \] contiene il componente su cui eseguire il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="d0135-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0135-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0135-111">Remarks</span></span>

<span data-ttu-id="d0135-112">Il formato del token contiene l'offset dell'istruzione endif corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="d0135-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="d0135-113">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="d0135-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="d0135-114">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="d0135-114">Restrictions</span></span>

-   <span data-ttu-id="d0135-115">Gli operandi di origine (se 4 vettori componenti) devono usare un singolo selettore di componenti.</span><span class="sxs-lookup"><span data-stu-id="d0135-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="d0135-116">Il registro a 32 bit fornito da *src0* viene testato a livello di bit.</span><span class="sxs-lookup"><span data-stu-id="d0135-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="d0135-117">Se un bit è diverso da zero, **se \_ z** sarà true.</span><span class="sxs-lookup"><span data-stu-id="d0135-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="d0135-118">Se tutti i bit sono zero, **se \_ NZ** sarà true.</span><span class="sxs-lookup"><span data-stu-id="d0135-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="d0135-119">I blocchi di controllo di flusso possono annidare fino a 64 di profondità per subroutine (e Main).</span><span class="sxs-lookup"><span data-stu-id="d0135-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="d0135-120">Il compilatore HLSL non genererà subroutine che superano questo limite.</span><span class="sxs-lookup"><span data-stu-id="d0135-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="d0135-121">Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità (per subroutine) non è definito.</span><span class="sxs-lookup"><span data-stu-id="d0135-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="d0135-122">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0135-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d0135-123">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="d0135-123">Vertex Shader</span></span> | <span data-ttu-id="d0135-124">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="d0135-124">Geometry Shader</span></span> | <span data-ttu-id="d0135-125">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="d0135-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d0135-126">x</span><span class="sxs-lookup"><span data-stu-id="d0135-126">x</span></span>             | <span data-ttu-id="d0135-127">x</span><span class="sxs-lookup"><span data-stu-id="d0135-127">x</span></span>               | <span data-ttu-id="d0135-128">x</span><span class="sxs-lookup"><span data-stu-id="d0135-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0135-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d0135-129">Minimum Shader Model</span></span>

<span data-ttu-id="d0135-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0135-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0135-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d0135-131">Shader Model</span></span>                                              | <span data-ttu-id="d0135-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="d0135-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d0135-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d0135-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d0135-134">sì</span><span class="sxs-lookup"><span data-stu-id="d0135-134">yes</span></span>       |
| [<span data-ttu-id="d0135-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="d0135-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d0135-136">sì</span><span class="sxs-lookup"><span data-stu-id="d0135-136">yes</span></span>       |
| [<span data-ttu-id="d0135-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d0135-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d0135-138">sì</span><span class="sxs-lookup"><span data-stu-id="d0135-138">yes</span></span>       |
| [<span data-ttu-id="d0135-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0135-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d0135-140">no</span><span class="sxs-lookup"><span data-stu-id="d0135-140">no</span></span>        |
| [<span data-ttu-id="d0135-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0135-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d0135-142">no</span><span class="sxs-lookup"><span data-stu-id="d0135-142">no</span></span>        |
| [<span data-ttu-id="d0135-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0135-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d0135-144">no</span><span class="sxs-lookup"><span data-stu-id="d0135-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d0135-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0135-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0135-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0135-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





