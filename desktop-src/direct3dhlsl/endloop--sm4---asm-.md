---
title: endloop (SM4-ASM)
description: Termina un'istruzione Loop.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398189"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="9c41f-103">endloop (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9c41f-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="9c41f-104">Termina un'istruzione Loop.</span><span class="sxs-lookup"><span data-stu-id="9c41f-104">Ends a loop statement.</span></span>



| <span data-ttu-id="9c41f-105">endloop</span><span class="sxs-lookup"><span data-stu-id="9c41f-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="9c41f-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c41f-106">Remarks</span></span>

<span data-ttu-id="9c41f-107">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="9c41f-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="9c41f-108">Il formato del token contiene l'offset dell'istruzione del ciclo corrispondente nello shader come praticità.</span><span class="sxs-lookup"><span data-stu-id="9c41f-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9c41f-109">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c41f-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c41f-110">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9c41f-110">Vertex Shader</span></span> | <span data-ttu-id="9c41f-111">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9c41f-111">Geometry Shader</span></span> | <span data-ttu-id="9c41f-112">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9c41f-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9c41f-113">x</span><span class="sxs-lookup"><span data-stu-id="9c41f-113">x</span></span>             | <span data-ttu-id="9c41f-114">x</span><span class="sxs-lookup"><span data-stu-id="9c41f-114">x</span></span>               | <span data-ttu-id="9c41f-115">x</span><span class="sxs-lookup"><span data-stu-id="9c41f-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c41f-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9c41f-116">Minimum Shader Model</span></span>

<span data-ttu-id="9c41f-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c41f-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9c41f-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9c41f-118">Shader Model</span></span>                                              | <span data-ttu-id="9c41f-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="9c41f-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c41f-120">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9c41f-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c41f-121">sì</span><span class="sxs-lookup"><span data-stu-id="9c41f-121">yes</span></span>       |
| [<span data-ttu-id="9c41f-122">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9c41f-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c41f-123">sì</span><span class="sxs-lookup"><span data-stu-id="9c41f-123">yes</span></span>       |
| [<span data-ttu-id="9c41f-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9c41f-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c41f-125">sì</span><span class="sxs-lookup"><span data-stu-id="9c41f-125">yes</span></span>       |
| [<span data-ttu-id="9c41f-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c41f-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c41f-127">no</span><span class="sxs-lookup"><span data-stu-id="9c41f-127">no</span></span>        |
| [<span data-ttu-id="9c41f-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c41f-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c41f-129">no</span><span class="sxs-lookup"><span data-stu-id="9c41f-129">no</span></span>        |
| [<span data-ttu-id="9c41f-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c41f-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c41f-131">no</span><span class="sxs-lookup"><span data-stu-id="9c41f-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c41f-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c41f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c41f-133">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c41f-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




