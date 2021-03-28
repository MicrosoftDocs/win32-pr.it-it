---
title: endif (SM4-ASM)
description: Termina un'istruzione if.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046056"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="67946-103">endif (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="67946-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="67946-104">Termina un'istruzione [if](if--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="67946-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="67946-105">endif</span><span class="sxs-lookup"><span data-stu-id="67946-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="67946-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="67946-106">Remarks</span></span>

<span data-ttu-id="67946-107">Nell'esempio seguente viene illustrato come utilizzare l'istruzione endif.</span><span class="sxs-lookup"><span data-stu-id="67946-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="67946-108">Il formato del token contiene l'offset dell'istruzione **if** corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="67946-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="67946-109">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="67946-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="67946-110">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="67946-110">Vertex Shader</span></span> | <span data-ttu-id="67946-111">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="67946-111">Geometry Shader</span></span> | <span data-ttu-id="67946-112">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="67946-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="67946-113">x</span><span class="sxs-lookup"><span data-stu-id="67946-113">x</span></span>             | <span data-ttu-id="67946-114">x</span><span class="sxs-lookup"><span data-stu-id="67946-114">x</span></span>               | <span data-ttu-id="67946-115">x</span><span class="sxs-lookup"><span data-stu-id="67946-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="67946-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="67946-116">Minimum Shader Model</span></span>

<span data-ttu-id="67946-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="67946-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="67946-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="67946-118">Shader Model</span></span>                                              | <span data-ttu-id="67946-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="67946-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="67946-120">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="67946-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="67946-121">sì</span><span class="sxs-lookup"><span data-stu-id="67946-121">yes</span></span>       |
| [<span data-ttu-id="67946-122">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="67946-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="67946-123">sì</span><span class="sxs-lookup"><span data-stu-id="67946-123">yes</span></span>       |
| [<span data-ttu-id="67946-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="67946-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="67946-125">sì</span><span class="sxs-lookup"><span data-stu-id="67946-125">yes</span></span>       |
| [<span data-ttu-id="67946-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67946-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="67946-127">no</span><span class="sxs-lookup"><span data-stu-id="67946-127">no</span></span>        |
| [<span data-ttu-id="67946-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67946-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="67946-129">no</span><span class="sxs-lookup"><span data-stu-id="67946-129">no</span></span>        |
| [<span data-ttu-id="67946-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67946-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="67946-131">no</span><span class="sxs-lookup"><span data-stu-id="67946-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="67946-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67946-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67946-133">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67946-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




