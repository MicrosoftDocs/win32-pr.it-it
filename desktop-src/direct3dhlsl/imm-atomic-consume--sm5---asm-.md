---
title: imm_atomic_consume (SM5-ASM)
description: Decrementa atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o accodare una visualizzazione di accesso non ordinato (UAV), restituendo il nuovo valore.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993128"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="b2837-103">\_utilizzo atomico \_ di IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b2837-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="b2837-104">Decrementa atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o accodare una visualizzazione di accesso non ordinato (UAV), restituendo il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="b2837-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="b2837-105">IMM \_ Atomic \_ USA dst0 \[ . Single \_ Component \_ mask \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="b2837-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="b2837-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2837-106">Item</span></span>                                                                                           | <span data-ttu-id="b2837-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2837-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b2837-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="b2837-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="b2837-109">\[in \] contiene il valore del contatore originale restituito.</span><span class="sxs-lookup"><span data-stu-id="b2837-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="b2837-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="b2837-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="b2837-111">\[in \] un buffer strutturato UAV con il flag count o Append.</span><span class="sxs-lookup"><span data-stu-id="b2837-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2837-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2837-112">Remarks</span></span>

<span data-ttu-id="b2837-113">Per una discussione sulla validità del valore del conteggio restituito, vedere l'argomento relativo alla presenza di un UAV in base al conteggio o all'accodamento. [ \_ \_ ](imm-atomic-alloc--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="b2837-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="b2837-114">Lo stesso vale per **l' \_ \_ utilizzo atomico di IMM**.</span><span class="sxs-lookup"><span data-stu-id="b2837-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="b2837-115">**IMM \_ Atomic \_ consume** esegue un decremento atomico del valore del contatore, restituendo il nuovo valore a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="b2837-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="b2837-116">Non è previsto alcun blocco del conteggio, quindi viene eseguito il wrapping in caso di underflow.</span><span class="sxs-lookup"><span data-stu-id="b2837-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="b2837-117">Lo stesso shader non è in grado di tentare di usare sia l' **\_ \_ allocazione** atomica di IMM che il **\_ \_ consumo atomico di IMM** nello stesso UAV.</span><span class="sxs-lookup"><span data-stu-id="b2837-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="b2837-118">Inoltre, la GPU non può consentire la combinazione di più chiamate shader per la combinazione di **IMM \_ Atomic \_ Alloc** e **IMM \_ Atomic \_ consume** nello stesso UAV.</span><span class="sxs-lookup"><span data-stu-id="b2837-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="b2837-119">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2837-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b2837-120">Vertice</span><span class="sxs-lookup"><span data-stu-id="b2837-120">Vertex</span></span> | <span data-ttu-id="b2837-121">Hull</span><span class="sxs-lookup"><span data-stu-id="b2837-121">Hull</span></span> | <span data-ttu-id="b2837-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="b2837-122">Domain</span></span> | <span data-ttu-id="b2837-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="b2837-123">Geometry</span></span> | <span data-ttu-id="b2837-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="b2837-124">Pixel</span></span> | <span data-ttu-id="b2837-125">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b2837-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b2837-126">X</span><span class="sxs-lookup"><span data-stu-id="b2837-126">X</span></span>     | <span data-ttu-id="b2837-127">X</span><span class="sxs-lookup"><span data-stu-id="b2837-127">X</span></span>       |



 

<span data-ttu-id="b2837-128">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b2837-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="b2837-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="b2837-129">Vertex</span></span> | <span data-ttu-id="b2837-130">Hull</span><span class="sxs-lookup"><span data-stu-id="b2837-130">Hull</span></span> | <span data-ttu-id="b2837-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="b2837-131">Domain</span></span> | <span data-ttu-id="b2837-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="b2837-132">Geometry</span></span> | <span data-ttu-id="b2837-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="b2837-133">Pixel</span></span> | <span data-ttu-id="b2837-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b2837-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b2837-135">X</span><span class="sxs-lookup"><span data-stu-id="b2837-135">X</span></span>      | <span data-ttu-id="b2837-136">X</span><span class="sxs-lookup"><span data-stu-id="b2837-136">X</span></span>    | <span data-ttu-id="b2837-137">X</span><span class="sxs-lookup"><span data-stu-id="b2837-137">X</span></span>      | <span data-ttu-id="b2837-138">X</span><span class="sxs-lookup"><span data-stu-id="b2837-138">X</span></span>        | <span data-ttu-id="b2837-139">X</span><span class="sxs-lookup"><span data-stu-id="b2837-139">X</span></span>     | <span data-ttu-id="b2837-140">X</span><span class="sxs-lookup"><span data-stu-id="b2837-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b2837-141">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b2837-141">Minimum Shader Model</span></span>

<span data-ttu-id="b2837-142">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2837-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b2837-143">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b2837-143">Shader Model</span></span>                                              | <span data-ttu-id="b2837-144">Supportato</span><span class="sxs-lookup"><span data-stu-id="b2837-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b2837-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b2837-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b2837-146">sì</span><span class="sxs-lookup"><span data-stu-id="b2837-146">yes</span></span>       |
| [<span data-ttu-id="b2837-147">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b2837-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b2837-148">no</span><span class="sxs-lookup"><span data-stu-id="b2837-148">no</span></span>        |
| [<span data-ttu-id="b2837-149">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b2837-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b2837-150">no</span><span class="sxs-lookup"><span data-stu-id="b2837-150">no</span></span>        |
| [<span data-ttu-id="b2837-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2837-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b2837-152">no</span><span class="sxs-lookup"><span data-stu-id="b2837-152">no</span></span>        |
| [<span data-ttu-id="b2837-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2837-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b2837-154">no</span><span class="sxs-lookup"><span data-stu-id="b2837-154">no</span></span>        |
| [<span data-ttu-id="b2837-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2837-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b2837-156">no</span><span class="sxs-lookup"><span data-stu-id="b2837-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b2837-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2837-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2837-158">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2837-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





