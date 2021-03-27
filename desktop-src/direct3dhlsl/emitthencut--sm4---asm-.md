---
title: emitThenCut (SM4-ASM)
description: Equivale a un comando Emit seguito da un comando Cut. | emitThenCut (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353861"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="554a6-104">emitThenCut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="554a6-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="554a6-105">Equivale a un comando [Emit](emit--sm4---asm-.md) seguito da un comando [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="554a6-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="554a6-106">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="554a6-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="554a6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="554a6-107">Remarks</span></span>

<span data-ttu-id="554a6-108">Questo comando è utile in caso di output noto dell'ultimo vertice in una topologia.</span><span class="sxs-lookup"><span data-stu-id="554a6-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="554a6-109">Se i flussi sono stati dichiarati, è necessario usare il [ \_ flusso emitthencut](emitthencut-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="554a6-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="554a6-110">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="554a6-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="554a6-111">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="554a6-111">Vertex Shader</span></span> | <span data-ttu-id="554a6-112">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="554a6-112">Geometry Shader</span></span> | <span data-ttu-id="554a6-113">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="554a6-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="554a6-114">x</span><span class="sxs-lookup"><span data-stu-id="554a6-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="554a6-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="554a6-115">Minimum Shader Model</span></span>

<span data-ttu-id="554a6-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="554a6-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="554a6-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="554a6-117">Shader Model</span></span>                                              | <span data-ttu-id="554a6-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="554a6-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="554a6-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="554a6-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="554a6-120">sì</span><span class="sxs-lookup"><span data-stu-id="554a6-120">yes</span></span>       |
| [<span data-ttu-id="554a6-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="554a6-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="554a6-122">sì</span><span class="sxs-lookup"><span data-stu-id="554a6-122">yes</span></span>       |
| [<span data-ttu-id="554a6-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="554a6-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="554a6-124">sì</span><span class="sxs-lookup"><span data-stu-id="554a6-124">yes</span></span>       |
| [<span data-ttu-id="554a6-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="554a6-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="554a6-126">no</span><span class="sxs-lookup"><span data-stu-id="554a6-126">no</span></span>        |
| [<span data-ttu-id="554a6-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="554a6-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="554a6-128">no</span><span class="sxs-lookup"><span data-stu-id="554a6-128">no</span></span>        |
| [<span data-ttu-id="554a6-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="554a6-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="554a6-130">no</span><span class="sxs-lookup"><span data-stu-id="554a6-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="554a6-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="554a6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="554a6-132">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="554a6-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




