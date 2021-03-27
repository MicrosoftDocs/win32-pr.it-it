---
title: cut_stream (SM5-ASM)
description: Istruzione Geometry shader che completa la topologia primitiva corrente nel flusso specificato, se è stato generato un vertice e avvia una nuova topologia del tipo dichiarato da Geometry shader in quel flusso.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398212"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="04da5-103">Taglia \_ flusso (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="04da5-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="04da5-104">Istruzione Geometry shader che completa la topologia primitiva corrente nel flusso specificato, se è stato generato un vertice e avvia una nuova topologia del tipo dichiarato da Geometry shader in quel flusso.</span><span class="sxs-lookup"><span data-stu-id="04da5-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="04da5-105">Taglia \_ streamIndex di flusso</span><span class="sxs-lookup"><span data-stu-id="04da5-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="04da5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="04da5-106">Item</span></span>                                                                                                               | <span data-ttu-id="04da5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04da5-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="04da5-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="04da5-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="04da5-109">\[nell' \] indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="04da5-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04da5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="04da5-110">Remarks</span></span>

<span data-ttu-id="04da5-111">Quando questa istruzione viene eseguita, tutte le topologie emesse in precedenza dalla chiamata geometry shader sono state completate.</span><span class="sxs-lookup"><span data-stu-id="04da5-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="04da5-112">Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="04da5-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="04da5-113">Poiché le uniche topologie di output disponibili per il geometry shader sono LineStrip e TriangleStrip, non ci sono mai vertici rimanenti.</span><span class="sxs-lookup"><span data-stu-id="04da5-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="04da5-114">*streamIndex* deve essere un valore immediato \[ 0.. 3 \] per un flusso dichiarato.</span><span class="sxs-lookup"><span data-stu-id="04da5-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="04da5-115">Dopo che la topologia precedente è stata completata, questa istruzione determina l'inizio di una nuova topologia, usando la topologia dichiarata come output per il geometry shader.</span><span class="sxs-lookup"><span data-stu-id="04da5-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="04da5-116">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="04da5-116">Restrictions</span></span>

-   <span data-ttu-id="04da5-117">Questa istruzione si applica solo a geometry shader.</span><span class="sxs-lookup"><span data-stu-id="04da5-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="04da5-118">il **Cut \_ Stream** può comparire un numero qualsiasi di volte nello shader Geometry, incluso all'interno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="04da5-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="04da5-119">Se il geometry shader termina e i vertici sono stati emessi, la topologia che compila viene completata, come se fosse stata eseguita un'istruzione **Cut \_ Stream** come ultima istruzione.</span><span class="sxs-lookup"><span data-stu-id="04da5-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="04da5-120">Se i flussi non sono stati dichiarati, è necessario usare [Cut](cut--sm4---asm-.md) anziché **Cut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="04da5-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="04da5-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="04da5-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="04da5-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="04da5-122">Vertex</span></span> | <span data-ttu-id="04da5-123">Hull</span><span class="sxs-lookup"><span data-stu-id="04da5-123">Hull</span></span> | <span data-ttu-id="04da5-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="04da5-124">Domain</span></span> | <span data-ttu-id="04da5-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="04da5-125">Geometry</span></span> | <span data-ttu-id="04da5-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="04da5-126">Pixel</span></span> | <span data-ttu-id="04da5-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="04da5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="04da5-128">X</span><span class="sxs-lookup"><span data-stu-id="04da5-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04da5-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="04da5-129">Minimum Shader Model</span></span>

<span data-ttu-id="04da5-130">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="04da5-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="04da5-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="04da5-131">Shader Model</span></span>                                              | <span data-ttu-id="04da5-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="04da5-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="04da5-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="04da5-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="04da5-134">sì</span><span class="sxs-lookup"><span data-stu-id="04da5-134">yes</span></span>       |
| [<span data-ttu-id="04da5-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="04da5-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="04da5-136">no</span><span class="sxs-lookup"><span data-stu-id="04da5-136">no</span></span>        |
| [<span data-ttu-id="04da5-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="04da5-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04da5-138">no</span><span class="sxs-lookup"><span data-stu-id="04da5-138">no</span></span>        |
| [<span data-ttu-id="04da5-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04da5-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04da5-140">no</span><span class="sxs-lookup"><span data-stu-id="04da5-140">no</span></span>        |
| [<span data-ttu-id="04da5-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04da5-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04da5-142">no</span><span class="sxs-lookup"><span data-stu-id="04da5-142">no</span></span>        |
| [<span data-ttu-id="04da5-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04da5-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04da5-144">no</span><span class="sxs-lookup"><span data-stu-id="04da5-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="04da5-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04da5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04da5-146">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04da5-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





