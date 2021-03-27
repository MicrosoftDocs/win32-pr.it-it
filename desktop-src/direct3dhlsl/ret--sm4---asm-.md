---
title: RET (SM4-ASM)
description: Istruzione return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719381"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="e7fcb-103">RET (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e7fcb-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="e7fcb-104">Istruzione return.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-104">Return statement.</span></span>



| <span data-ttu-id="e7fcb-105">RET</span><span class="sxs-lookup"><span data-stu-id="e7fcb-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="e7fcb-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7fcb-106">Remarks</span></span>

<span data-ttu-id="e7fcb-107">Se all'interno di una subroutine, tornare all'istruzione dopo la chiamata a.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="e7fcb-108">In caso contrario, terminare l'esecuzione del programma.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="e7fcb-109">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="e7fcb-110">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="e7fcb-110">Restrictions</span></span>

-   <span data-ttu-id="e7fcb-111">**ret** può trovarsi in qualsiasi punto di un programma, un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="e7fcb-112">Se un'istruzione [Label](label--sm4---asm-.md) viene visualizzata in uno shader, deve essere preceduta da un comando **ret** che non è annidato in alcuna istruzione di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="e7fcb-113">Se sono presenti subroutine in uno shader, l'ultima istruzione nello shader deve essere **ret**.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="e7fcb-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7fcb-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e7fcb-115">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="e7fcb-115">Vertex Shader</span></span> | <span data-ttu-id="e7fcb-116">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="e7fcb-116">Geometry Shader</span></span> | <span data-ttu-id="e7fcb-117">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="e7fcb-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e7fcb-118">x</span><span class="sxs-lookup"><span data-stu-id="e7fcb-118">x</span></span>             | <span data-ttu-id="e7fcb-119">x</span><span class="sxs-lookup"><span data-stu-id="e7fcb-119">x</span></span>               | <span data-ttu-id="e7fcb-120">x</span><span class="sxs-lookup"><span data-stu-id="e7fcb-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e7fcb-121">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e7fcb-121">Minimum Shader Model</span></span>

<span data-ttu-id="e7fcb-122">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7fcb-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e7fcb-123">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e7fcb-123">Shader Model</span></span>                                              | <span data-ttu-id="e7fcb-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="e7fcb-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e7fcb-125">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e7fcb-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e7fcb-126">sì</span><span class="sxs-lookup"><span data-stu-id="e7fcb-126">yes</span></span>       |
| [<span data-ttu-id="e7fcb-127">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e7fcb-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e7fcb-128">sì</span><span class="sxs-lookup"><span data-stu-id="e7fcb-128">yes</span></span>       |
| [<span data-ttu-id="e7fcb-129">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e7fcb-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e7fcb-130">sì</span><span class="sxs-lookup"><span data-stu-id="e7fcb-130">yes</span></span>       |
| [<span data-ttu-id="e7fcb-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7fcb-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e7fcb-132">no</span><span class="sxs-lookup"><span data-stu-id="e7fcb-132">no</span></span>        |
| [<span data-ttu-id="e7fcb-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7fcb-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e7fcb-134">no</span><span class="sxs-lookup"><span data-stu-id="e7fcb-134">no</span></span>        |
| [<span data-ttu-id="e7fcb-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7fcb-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e7fcb-136">no</span><span class="sxs-lookup"><span data-stu-id="e7fcb-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e7fcb-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7fcb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7fcb-138">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7fcb-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




