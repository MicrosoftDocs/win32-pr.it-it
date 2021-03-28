---
title: Break (SM4-ASM)
description: Sposta il punto di esecuzione nell'istruzione dopo il EndLoop o endswitch successivo.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335511"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="8d7e9-103">Break (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d7e9-103">break (sm4 - asm)</span></span>

<span data-ttu-id="8d7e9-104">Sposta il punto di esecuzione nell'istruzione dopo il [EndLoop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md)successivo.</span><span class="sxs-lookup"><span data-stu-id="8d7e9-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="8d7e9-105">break</span><span class="sxs-lookup"><span data-stu-id="8d7e9-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="8d7e9-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d7e9-106">Remarks</span></span>

<span data-ttu-id="8d7e9-107">Il formato del token contiene l'offset dell'istruzione **EndLoop** o **endswitch** corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="8d7e9-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="8d7e9-108">Nell'esempio seguente viene illustrata l'istruzione **break** .</span><span class="sxs-lookup"><span data-stu-id="8d7e9-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="8d7e9-109">Questa istruzione deve essere visualizzata all'interno di un **ciclo** / **EndLoop** o in un **caso** in un  / **endswitch** switch.</span><span class="sxs-lookup"><span data-stu-id="8d7e9-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="8d7e9-110">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d7e9-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d7e9-111">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="8d7e9-111">Vertex Shader</span></span> | <span data-ttu-id="8d7e9-112">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="8d7e9-112">Geometry Shader</span></span> | <span data-ttu-id="8d7e9-113">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="8d7e9-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8d7e9-114">x</span><span class="sxs-lookup"><span data-stu-id="8d7e9-114">x</span></span>             | <span data-ttu-id="8d7e9-115">x</span><span class="sxs-lookup"><span data-stu-id="8d7e9-115">x</span></span>               | <span data-ttu-id="8d7e9-116">x</span><span class="sxs-lookup"><span data-stu-id="8d7e9-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d7e9-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8d7e9-117">Minimum Shader Model</span></span>

<span data-ttu-id="8d7e9-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8d7e9-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d7e9-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8d7e9-119">Shader Model</span></span>                                              | <span data-ttu-id="8d7e9-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="8d7e9-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d7e9-121">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8d7e9-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d7e9-122">sì</span><span class="sxs-lookup"><span data-stu-id="8d7e9-122">yes</span></span>       |
| [<span data-ttu-id="8d7e9-123">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8d7e9-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d7e9-124">sì</span><span class="sxs-lookup"><span data-stu-id="8d7e9-124">yes</span></span>       |
| [<span data-ttu-id="8d7e9-125">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8d7e9-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d7e9-126">sì</span><span class="sxs-lookup"><span data-stu-id="8d7e9-126">yes</span></span>       |
| [<span data-ttu-id="8d7e9-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7e9-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d7e9-128">no</span><span class="sxs-lookup"><span data-stu-id="8d7e9-128">no</span></span>        |
| [<span data-ttu-id="8d7e9-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7e9-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d7e9-130">no</span><span class="sxs-lookup"><span data-stu-id="8d7e9-130">no</span></span>        |
| [<span data-ttu-id="8d7e9-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7e9-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d7e9-132">no</span><span class="sxs-lookup"><span data-stu-id="8d7e9-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d7e9-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d7e9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d7e9-134">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7e9-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




