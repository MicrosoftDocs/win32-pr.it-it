---
title: Saturate (riferimento HLSL)
description: Consente di bloccare il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia a \ 0,0 f... 1,0 f \ intervallo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398336"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="e4f10-103">Saturate (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4f10-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="e4f10-104">Consente di bloccare il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia a \[ 0,0 f... 1,0 f \] intervallo.</span><span class="sxs-lookup"><span data-stu-id="e4f10-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="e4f10-105">\_Sat</span><span class="sxs-lookup"><span data-stu-id="e4f10-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="e4f10-106">Il modificatore di risultato dell'istruzione **saturate** esegue l'operazione seguente sui valori dei risultati da un'operazione aritmetica a virgola mobile a cui è stato \_ applicato il Sab:</span><span class="sxs-lookup"><span data-stu-id="e4f10-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="e4f10-107">dove min () e Max () nell'espressione precedente si comportano nel modo in cui [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)o [DMax](dmax--sm5---asm-.md) operano.</span><span class="sxs-lookup"><span data-stu-id="e4f10-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="e4f10-108">`_sat(NaN)` restituisce 0, in base alle regole per min e max.</span><span class="sxs-lookup"><span data-stu-id="e4f10-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e4f10-109">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e4f10-109">Minimum Shader Model</span></span>

<span data-ttu-id="e4f10-110">Questo modificatore è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4f10-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="e4f10-111">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e4f10-111">Shader Model</span></span>                                              | <span data-ttu-id="e4f10-112">Supportato</span><span class="sxs-lookup"><span data-stu-id="e4f10-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e4f10-113">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e4f10-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e4f10-114">sì</span><span class="sxs-lookup"><span data-stu-id="e4f10-114">yes</span></span>       |
| [<span data-ttu-id="e4f10-115">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e4f10-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e4f10-116">sì</span><span class="sxs-lookup"><span data-stu-id="e4f10-116">yes</span></span>       |
| [<span data-ttu-id="e4f10-117">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e4f10-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e4f10-118">sì</span><span class="sxs-lookup"><span data-stu-id="e4f10-118">yes</span></span>       |
| [<span data-ttu-id="e4f10-119">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4f10-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e4f10-120">no</span><span class="sxs-lookup"><span data-stu-id="e4f10-120">no</span></span>        |
| [<span data-ttu-id="e4f10-121">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4f10-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e4f10-122">no</span><span class="sxs-lookup"><span data-stu-id="e4f10-122">no</span></span>        |
| [<span data-ttu-id="e4f10-123">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4f10-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e4f10-124">no</span><span class="sxs-lookup"><span data-stu-id="e4f10-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e4f10-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4f10-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f10-126">Modificatori di istruzione</span><span class="sxs-lookup"><span data-stu-id="e4f10-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




