---
title: emit_stream (SM5-ASM)
description: Creare un vertice in un flusso specificato.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398229"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="dc20c-103">Emit \_ Stream (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="dc20c-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="dc20c-104">Creare un vertice in un flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="dc20c-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="dc20c-105">genera \_ flusso streamIndex</span><span class="sxs-lookup"><span data-stu-id="dc20c-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="dc20c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dc20c-106">Item</span></span>                                                                                                               | <span data-ttu-id="dc20c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc20c-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="dc20c-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="dc20c-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="dc20c-109">\[nell' \] indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="dc20c-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc20c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc20c-110">Remarks</span></span>

<span data-ttu-id="dc20c-111">Questa istruzione causa la lettura da parte di Geometry shader di tutti i registri o dichiarati \# per il flusso specificato per generare un vertice.</span><span class="sxs-lookup"><span data-stu-id="dc20c-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="dc20c-112">Dopo l'emissione, tutti i dati in tutti i registri di output per tutti i flussi diventano non inizializzati, non solo il flusso generato a.</span><span class="sxs-lookup"><span data-stu-id="dc20c-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="dc20c-113">*streamIndex* deve essere un valore immediato \[ 0.. 3 \] per un flusso dichiarato.</span><span class="sxs-lookup"><span data-stu-id="dc20c-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="dc20c-114">Quando vengono rilasciate più chiamate a **\_ flussi Emit** , vengono generate le primitive.</span><span class="sxs-lookup"><span data-stu-id="dc20c-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="dc20c-115">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="dc20c-115">Restrictions</span></span>

-   <span data-ttu-id="dc20c-116">**il \_ flusso di emissione** può comparire un numero qualsiasi di volte in un geometry shader, incluso all'interno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="dc20c-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="dc20c-117">Se i flussi non sono stati dichiarati, è necessario usare [Emit](emit--sm4---asm-.md) anziché **Emit \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="dc20c-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="dc20c-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc20c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dc20c-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="dc20c-119">Vertex</span></span> | <span data-ttu-id="dc20c-120">Hull</span><span class="sxs-lookup"><span data-stu-id="dc20c-120">Hull</span></span> | <span data-ttu-id="dc20c-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="dc20c-121">Domain</span></span> | <span data-ttu-id="dc20c-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="dc20c-122">Geometry</span></span> | <span data-ttu-id="dc20c-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="dc20c-123">Pixel</span></span> | <span data-ttu-id="dc20c-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dc20c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="dc20c-125">X</span><span class="sxs-lookup"><span data-stu-id="dc20c-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dc20c-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="dc20c-126">Minimum Shader Model</span></span>

<span data-ttu-id="dc20c-127">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc20c-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="dc20c-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="dc20c-128">Shader Model</span></span>                                              | <span data-ttu-id="dc20c-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="dc20c-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dc20c-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dc20c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dc20c-131">sì</span><span class="sxs-lookup"><span data-stu-id="dc20c-131">yes</span></span>       |
| [<span data-ttu-id="dc20c-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="dc20c-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dc20c-133">no</span><span class="sxs-lookup"><span data-stu-id="dc20c-133">no</span></span>        |
| [<span data-ttu-id="dc20c-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="dc20c-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dc20c-135">no</span><span class="sxs-lookup"><span data-stu-id="dc20c-135">no</span></span>        |
| [<span data-ttu-id="dc20c-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dc20c-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dc20c-137">no</span><span class="sxs-lookup"><span data-stu-id="dc20c-137">no</span></span>        |
| [<span data-ttu-id="dc20c-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dc20c-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dc20c-139">no</span><span class="sxs-lookup"><span data-stu-id="dc20c-139">no</span></span>        |
| [<span data-ttu-id="dc20c-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dc20c-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dc20c-141">no</span><span class="sxs-lookup"><span data-stu-id="dc20c-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dc20c-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc20c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc20c-143">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dc20c-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





