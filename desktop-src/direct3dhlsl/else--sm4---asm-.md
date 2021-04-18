---
title: Else (SM4-ASM)
description: Avvia un blocco else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976458"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="0f109-103">Else (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0f109-103">else (sm4 - asm)</span></span>

<span data-ttu-id="0f109-104">Avvia un blocco **else** .</span><span class="sxs-lookup"><span data-stu-id="0f109-104">Starts an **else** block.</span></span>



| <span data-ttu-id="0f109-105">else</span><span class="sxs-lookup"><span data-stu-id="0f109-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="0f109-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f109-106">Remarks</span></span>

<span data-ttu-id="0f109-107">Il formato del token contiene l'offset dell'istruzione [endif](endif--sm4---asm-.md) corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="0f109-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="0f109-108">Nell'esempio seguente viene illustrato come utilizzare l'istruzione **else** .</span><span class="sxs-lookup"><span data-stu-id="0f109-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="0f109-109">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f109-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f109-110">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0f109-110">Vertex Shader</span></span> | <span data-ttu-id="0f109-111">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="0f109-111">Geometry Shader</span></span> | <span data-ttu-id="0f109-112">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="0f109-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0f109-113">x</span><span class="sxs-lookup"><span data-stu-id="0f109-113">x</span></span>             | <span data-ttu-id="0f109-114">x</span><span class="sxs-lookup"><span data-stu-id="0f109-114">x</span></span>               | <span data-ttu-id="0f109-115">x</span><span class="sxs-lookup"><span data-stu-id="0f109-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f109-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0f109-116">Minimum Shader Model</span></span>

<span data-ttu-id="0f109-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0f109-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f109-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0f109-118">Shader Model</span></span>                                              | <span data-ttu-id="0f109-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="0f109-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f109-120">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0f109-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f109-121">sì</span><span class="sxs-lookup"><span data-stu-id="0f109-121">yes</span></span>       |
| [<span data-ttu-id="0f109-122">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="0f109-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f109-123">sì</span><span class="sxs-lookup"><span data-stu-id="0f109-123">yes</span></span>       |
| [<span data-ttu-id="0f109-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0f109-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f109-125">sì</span><span class="sxs-lookup"><span data-stu-id="0f109-125">yes</span></span>       |
| [<span data-ttu-id="0f109-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f109-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f109-127">no</span><span class="sxs-lookup"><span data-stu-id="0f109-127">no</span></span>        |
| [<span data-ttu-id="0f109-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f109-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f109-129">no</span><span class="sxs-lookup"><span data-stu-id="0f109-129">no</span></span>        |
| [<span data-ttu-id="0f109-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f109-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f109-131">no</span><span class="sxs-lookup"><span data-stu-id="0f109-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f109-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f109-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f109-133">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f109-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




