---
title: loop (SM4-ASM)
description: Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione break.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993104"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="2a638-103">loop (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2a638-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="2a638-104">Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione break.</span><span class="sxs-lookup"><span data-stu-id="2a638-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="2a638-105">loop</span><span class="sxs-lookup"><span data-stu-id="2a638-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="2a638-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a638-106">Remarks</span></span>

<span data-ttu-id="2a638-107">il **ciclo** può scorrere a tempo indefinito, sebbene l'esecuzione complessiva dello shader possa essere forzata per terminare dopo l'esecuzione di un certo numero di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="2a638-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="2a638-108">I blocchi di controllo di flusso possono annidare fino a 64 di profondità per subroutine e Main.</span><span class="sxs-lookup"><span data-stu-id="2a638-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="2a638-109">Il compilatore HLSL non genererà subroutine che superano questo limite.</span><span class="sxs-lookup"><span data-stu-id="2a638-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="2a638-110">Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità per subroutine non è definito.</span><span class="sxs-lookup"><span data-stu-id="2a638-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="2a638-111">Il formato del token contiene l'offset dell'istruzione [EndLoop](endloop--sm4---asm-.md) corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="2a638-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="2a638-112">Nell'esempio seguente viene illustrato come utilizzare l'istruzione Loop.</span><span class="sxs-lookup"><span data-stu-id="2a638-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="2a638-113">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a638-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2a638-114">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2a638-114">Vertex Shader</span></span> | <span data-ttu-id="2a638-115">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2a638-115">Geometry Shader</span></span> | <span data-ttu-id="2a638-116">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2a638-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2a638-117">x</span><span class="sxs-lookup"><span data-stu-id="2a638-117">x</span></span>             | <span data-ttu-id="2a638-118">x</span><span class="sxs-lookup"><span data-stu-id="2a638-118">x</span></span>               | <span data-ttu-id="2a638-119">x</span><span class="sxs-lookup"><span data-stu-id="2a638-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2a638-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2a638-120">Minimum Shader Model</span></span>

<span data-ttu-id="2a638-121">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a638-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2a638-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2a638-122">Shader Model</span></span>                                              | <span data-ttu-id="2a638-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="2a638-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2a638-124">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2a638-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2a638-125">sì</span><span class="sxs-lookup"><span data-stu-id="2a638-125">yes</span></span>       |
| [<span data-ttu-id="2a638-126">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2a638-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2a638-127">sì</span><span class="sxs-lookup"><span data-stu-id="2a638-127">yes</span></span>       |
| [<span data-ttu-id="2a638-128">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2a638-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2a638-129">sì</span><span class="sxs-lookup"><span data-stu-id="2a638-129">yes</span></span>       |
| [<span data-ttu-id="2a638-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a638-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2a638-131">no</span><span class="sxs-lookup"><span data-stu-id="2a638-131">no</span></span>        |
| [<span data-ttu-id="2a638-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a638-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2a638-133">no</span><span class="sxs-lookup"><span data-stu-id="2a638-133">no</span></span>        |
| [<span data-ttu-id="2a638-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a638-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2a638-135">no</span><span class="sxs-lookup"><span data-stu-id="2a638-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2a638-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a638-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a638-137">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a638-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




