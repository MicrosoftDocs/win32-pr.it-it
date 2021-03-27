---
title: Emit (SM4-ASM)
description: Creare un vertice.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719357"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="1f837-103">Emit (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1f837-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="1f837-104">Creare un vertice.</span><span class="sxs-lookup"><span data-stu-id="1f837-104">Emit a vertex.</span></span>



| <span data-ttu-id="1f837-105">Emit</span><span class="sxs-lookup"><span data-stu-id="1f837-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="1f837-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f837-106">Remarks</span></span>

<span data-ttu-id="1f837-107">**Emit** causa la lettura da parte di Geometry shader di tutti i registri o dichiarati per \# generare un vertice.</span><span class="sxs-lookup"><span data-stu-id="1f837-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="1f837-108">Quando vengono emesse più chiamate **Emit** , vengono generate le primitive.</span><span class="sxs-lookup"><span data-stu-id="1f837-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="1f837-109">**Emit** può apparire un numero qualsiasi di volte in un geometry shader, incluso all'interno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="1f837-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="1f837-110">Se i flussi sono stati dichiarati, è necessario usare il [ \_ flusso di emissione](emit-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="1f837-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="1f837-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f837-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1f837-112">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="1f837-112">Vertex Shader</span></span> | <span data-ttu-id="1f837-113">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="1f837-113">Geometry Shader</span></span> | <span data-ttu-id="1f837-114">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="1f837-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="1f837-115">x</span><span class="sxs-lookup"><span data-stu-id="1f837-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="1f837-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="1f837-116">Minimum Shader Model</span></span>

<span data-ttu-id="1f837-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f837-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1f837-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="1f837-118">Shader Model</span></span>                                              | <span data-ttu-id="1f837-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="1f837-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1f837-120">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="1f837-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1f837-121">sì</span><span class="sxs-lookup"><span data-stu-id="1f837-121">yes</span></span>       |
| [<span data-ttu-id="1f837-122">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="1f837-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1f837-123">sì</span><span class="sxs-lookup"><span data-stu-id="1f837-123">yes</span></span>       |
| [<span data-ttu-id="1f837-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="1f837-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1f837-125">sì</span><span class="sxs-lookup"><span data-stu-id="1f837-125">yes</span></span>       |
| [<span data-ttu-id="1f837-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f837-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1f837-127">no</span><span class="sxs-lookup"><span data-stu-id="1f837-127">no</span></span>        |
| [<span data-ttu-id="1f837-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f837-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1f837-129">no</span><span class="sxs-lookup"><span data-stu-id="1f837-129">no</span></span>        |
| [<span data-ttu-id="1f837-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f837-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1f837-131">no</span><span class="sxs-lookup"><span data-stu-id="1f837-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1f837-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f837-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f837-133">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f837-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




