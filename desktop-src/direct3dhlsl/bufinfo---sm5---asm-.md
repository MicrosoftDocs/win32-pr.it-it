---
title: bufinfo (SM5-ASM)
description: Eseguire una query sul numero di elementi in un buffer (ma non sul buffer costante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993077"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="95248-103">bufinfo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="95248-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="95248-104">Eseguire una query sul numero di elementi in un buffer (ma non sul buffer costante).</span><span class="sxs-lookup"><span data-stu-id="95248-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="95248-105">bufinfo dest \[ . mask \] , srcResource</span><span class="sxs-lookup"><span data-stu-id="95248-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="95248-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="95248-106">Item</span></span>                                                                                                               | <span data-ttu-id="95248-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95248-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95248-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="95248-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="95248-109">\[nell' \] indirizzo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="95248-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="95248-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="95248-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="95248-111">\[nel \] buffer, diverso da un buffer costante, in un SRV (t \# ) o in un UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="95248-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95248-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="95248-112">Remarks</span></span>

<span data-ttu-id="95248-113">Tutti i componenti in *dest* ricevono il numero intero di elementi nella visualizzazione delle risorse dello shader del buffer.</span><span class="sxs-lookup"><span data-stu-id="95248-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="95248-114">Il numero di elementi dipende dai parametri di visualizzazione, ad esempio il formato della memoria.</span><span class="sxs-lookup"><span data-stu-id="95248-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="95248-115">Per un buffer tipizzato SRV o UAV, il valore restituito è il numero di elementi nella visualizzazione (in cui un elemento è un'unità del formato tipizzato).</span><span class="sxs-lookup"><span data-stu-id="95248-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="95248-116">Per un buffer non elaborato SRV o UAV, il valore restituito è il numero di byte nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="95248-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="95248-117">Per un buffer strutturato SRV o UAV, il valore restituito è il numero di strutture nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="95248-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="95248-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="95248-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="95248-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="95248-119">Vertex</span></span> | <span data-ttu-id="95248-120">Hull</span><span class="sxs-lookup"><span data-stu-id="95248-120">Hull</span></span> | <span data-ttu-id="95248-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="95248-121">Domain</span></span> | <span data-ttu-id="95248-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="95248-122">Geometry</span></span> | <span data-ttu-id="95248-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="95248-123">Pixel</span></span> | <span data-ttu-id="95248-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="95248-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="95248-125">X</span><span class="sxs-lookup"><span data-stu-id="95248-125">X</span></span>      | <span data-ttu-id="95248-126">X</span><span class="sxs-lookup"><span data-stu-id="95248-126">X</span></span>    | <span data-ttu-id="95248-127">X</span><span class="sxs-lookup"><span data-stu-id="95248-127">X</span></span>      | <span data-ttu-id="95248-128">X</span><span class="sxs-lookup"><span data-stu-id="95248-128">X</span></span>        | <span data-ttu-id="95248-129">X</span><span class="sxs-lookup"><span data-stu-id="95248-129">X</span></span>     | <span data-ttu-id="95248-130">X</span><span class="sxs-lookup"><span data-stu-id="95248-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="95248-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="95248-131">Minimum Shader Model</span></span>

<span data-ttu-id="95248-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="95248-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="95248-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="95248-133">Shader Model</span></span>                                              | <span data-ttu-id="95248-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="95248-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="95248-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="95248-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="95248-136">sì</span><span class="sxs-lookup"><span data-stu-id="95248-136">yes</span></span>       |
| [<span data-ttu-id="95248-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="95248-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="95248-138">no</span><span class="sxs-lookup"><span data-stu-id="95248-138">no</span></span>        |
| [<span data-ttu-id="95248-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="95248-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="95248-140">no</span><span class="sxs-lookup"><span data-stu-id="95248-140">no</span></span>        |
| [<span data-ttu-id="95248-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95248-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="95248-142">no</span><span class="sxs-lookup"><span data-stu-id="95248-142">no</span></span>        |
| [<span data-ttu-id="95248-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95248-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="95248-144">no</span><span class="sxs-lookup"><span data-stu-id="95248-144">no</span></span>        |
| [<span data-ttu-id="95248-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95248-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="95248-146">no</span><span class="sxs-lookup"><span data-stu-id="95248-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="95248-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95248-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95248-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95248-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





