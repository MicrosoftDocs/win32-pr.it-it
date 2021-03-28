---
title: endswitch (SM4-ASM)
description: Termina un'istruzione switch.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398188"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="b7f8c-103">endswitch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="b7f8c-104">Termina un'istruzione [Switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f8c-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="b7f8c-105">endswitch</span><span class="sxs-lookup"><span data-stu-id="b7f8c-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="b7f8c-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7f8c-106">Remarks</span></span>

<span data-ttu-id="b7f8c-107">Il formato del token contiene l'offset dell'istruzione switch corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="b7f8c-108">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7f8c-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7f8c-109">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="b7f8c-109">Vertex Shader</span></span> | <span data-ttu-id="b7f8c-110">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="b7f8c-110">Geometry Shader</span></span> | <span data-ttu-id="b7f8c-111">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="b7f8c-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b7f8c-112">x</span><span class="sxs-lookup"><span data-stu-id="b7f8c-112">x</span></span>             | <span data-ttu-id="b7f8c-113">x</span><span class="sxs-lookup"><span data-stu-id="b7f8c-113">x</span></span>               | <span data-ttu-id="b7f8c-114">x</span><span class="sxs-lookup"><span data-stu-id="b7f8c-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7f8c-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b7f8c-115">Minimum Shader Model</span></span>

<span data-ttu-id="b7f8c-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7f8c-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b7f8c-117">Shader Model</span></span>                                              | <span data-ttu-id="b7f8c-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="b7f8c-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7f8c-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b7f8c-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7f8c-120">sì</span><span class="sxs-lookup"><span data-stu-id="b7f8c-120">yes</span></span>       |
| [<span data-ttu-id="b7f8c-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b7f8c-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7f8c-122">sì</span><span class="sxs-lookup"><span data-stu-id="b7f8c-122">yes</span></span>       |
| [<span data-ttu-id="b7f8c-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b7f8c-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7f8c-124">sì</span><span class="sxs-lookup"><span data-stu-id="b7f8c-124">yes</span></span>       |
| [<span data-ttu-id="b7f8c-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7f8c-126">no</span><span class="sxs-lookup"><span data-stu-id="b7f8c-126">no</span></span>        |
| [<span data-ttu-id="b7f8c-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7f8c-128">no</span><span class="sxs-lookup"><span data-stu-id="b7f8c-128">no</span></span>        |
| [<span data-ttu-id="b7f8c-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7f8c-130">no</span><span class="sxs-lookup"><span data-stu-id="b7f8c-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7f8c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7f8c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f8c-132">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




