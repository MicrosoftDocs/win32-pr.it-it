---
title: Cut (SM4-ASM)
description: Istruzione Geometry shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry shader.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976327"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="d79b0-103">Cut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d79b0-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="d79b0-104">Istruzione Geometry shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d79b0-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="d79b0-105">tagliare</span><span class="sxs-lookup"><span data-stu-id="d79b0-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="d79b0-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="d79b0-106">Remarks</span></span>

<span data-ttu-id="d79b0-107">Quando si esegue il **Cut** , la prima cosa che si verifica è che tutte le topologie generate in precedenza dalla chiamata geometry shader siano state completate.</span><span class="sxs-lookup"><span data-stu-id="d79b0-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="d79b0-108">Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="d79b0-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="d79b0-109">Poiché le uniche topologie di output disponibili per il geometry shader sono LineStrip e TriangleStrip, non ci sono mai vertici rimanenti al momento dell' **interruzione**.</span><span class="sxs-lookup"><span data-stu-id="d79b0-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="d79b0-110">Dopo che la topologia precedente è stata completata, **Cut** causa l'inizio di una nuova topologia, usando la topologia dichiarata come output di Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d79b0-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="d79b0-111">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="d79b0-111">Restrictions</span></span>

-   <span data-ttu-id="d79b0-112">L'istruzione **Cut** si applica solo a geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d79b0-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="d79b0-113">il **taglio** può apparire un numero qualsiasi di volte nello shader Geometry, incluso all'interno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="d79b0-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="d79b0-114">Se il geometry shader termina e i vertici sono stati emessi, la topologia che compila viene completata, come se fosse stato eseguito un **taglio** come ultima istruzione.</span><span class="sxs-lookup"><span data-stu-id="d79b0-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="d79b0-115">Se i flussi sono stati dichiarati, è necessario usare [Cut \_ Stream](cut-stream---sm5---asm-.md) anziché **Cut**.</span><span class="sxs-lookup"><span data-stu-id="d79b0-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="d79b0-116">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d79b0-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d79b0-117">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="d79b0-117">Vertex Shader</span></span> | <span data-ttu-id="d79b0-118">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="d79b0-118">Geometry Shader</span></span> | <span data-ttu-id="d79b0-119">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="d79b0-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="d79b0-120">x</span><span class="sxs-lookup"><span data-stu-id="d79b0-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d79b0-121">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d79b0-121">Minimum Shader Model</span></span>

<span data-ttu-id="d79b0-122">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d79b0-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d79b0-123">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d79b0-123">Shader Model</span></span>                                              | <span data-ttu-id="d79b0-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="d79b0-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d79b0-125">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d79b0-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d79b0-126">sì</span><span class="sxs-lookup"><span data-stu-id="d79b0-126">yes</span></span>       |
| [<span data-ttu-id="d79b0-127">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="d79b0-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d79b0-128">sì</span><span class="sxs-lookup"><span data-stu-id="d79b0-128">yes</span></span>       |
| [<span data-ttu-id="d79b0-129">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d79b0-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d79b0-130">sì</span><span class="sxs-lookup"><span data-stu-id="d79b0-130">yes</span></span>       |
| [<span data-ttu-id="d79b0-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d79b0-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d79b0-132">no</span><span class="sxs-lookup"><span data-stu-id="d79b0-132">no</span></span>        |
| [<span data-ttu-id="d79b0-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d79b0-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d79b0-134">no</span><span class="sxs-lookup"><span data-stu-id="d79b0-134">no</span></span>        |
| [<span data-ttu-id="d79b0-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d79b0-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d79b0-136">no</span><span class="sxs-lookup"><span data-stu-id="d79b0-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d79b0-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d79b0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d79b0-138">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d79b0-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




