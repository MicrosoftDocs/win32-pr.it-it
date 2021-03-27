---
title: imm_atomic_alloc (SM5-ASM)
description: Incrementare atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o aggiungere la visualizzazione di accesso non ordinato (UAV), restituendo il valore originale.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719426"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="f7218-103">IMM \_ Atomic \_ Alloc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f7218-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="f7218-104">Incrementare atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o aggiungere la visualizzazione di accesso non ordinato (UAV), restituendo il valore originale.</span><span class="sxs-lookup"><span data-stu-id="f7218-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="f7218-105">IMM \_ Atomic \_ Alloc dst0 \[ . Single \_ Component \_ mask \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="f7218-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="f7218-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7218-106">Item</span></span>                                                                                           | <span data-ttu-id="f7218-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7218-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f7218-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f7218-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="f7218-109">\[in \] contiene il valore del contatore restituito.</span><span class="sxs-lookup"><span data-stu-id="f7218-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="f7218-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="f7218-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="f7218-111">\[in \] un buffer strutturato UAV con il flag count o Append.</span><span class="sxs-lookup"><span data-stu-id="f7218-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7218-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7218-112">Remarks</span></span>

<span data-ttu-id="f7218-113">È presente un valore di contatore intero senza segno a 32 bit nascosto associato a ogni conteggio o visualizzazione buffer di Accodamento, che viene inizializzato quando la vista è associata alla pipeline, inclusa l'opzione per il mantenimento del valore precedente.</span><span class="sxs-lookup"><span data-stu-id="f7218-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="f7218-114">Questa istruzione esegue un incremento atomico del valore del contatore, restituendo l'originale a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="f7218-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="f7218-115">Per un UAV Append, il valore restituito è valido solo per la durata della chiamata dello shader.</span><span class="sxs-lookup"><span data-stu-id="f7218-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="f7218-116">Successivamente, l'implementazione può riorganizzare il layout di memoria.</span><span class="sxs-lookup"><span data-stu-id="f7218-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="f7218-117">Tutti gli indirizzi di memoria basati sul valore restituito devono essere limitati alla chiamata dello shader.</span><span class="sxs-lookup"><span data-stu-id="f7218-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="f7218-118">Per un UAV Append, all'interno della chiamata dello shader il compilatore HLSL può usare il valore restituito come indice struct da usare per l'accesso al buffer strutturato.</span><span class="sxs-lookup"><span data-stu-id="f7218-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="f7218-119">L'accesso a qualsiasi indice struct diverso da quello restituito dalle chiamate a **IMM \_ Atomic \_ Alloc** o [ \_ consume](imm-atomic-consume--sm5---asm-.md) genera risultati non definiti in quanto la posizione di memoria all'interno del UAV viene eseguita in modo casuale e fissa solo per la durata della chiamata dello shader.</span><span class="sxs-lookup"><span data-stu-id="f7218-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="f7218-120">Per un numero UAV, il valore restituito può essere salvato dall'applicazione come riferimento a un percorso fisso all'interno del UAV che è significativo dopo la chiamata dello shader.</span><span class="sxs-lookup"><span data-stu-id="f7218-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="f7218-121">È possibile accedere sempre a qualsiasi posizione in un UAV di conteggio indipendentemente dal valore del conteggio.</span><span class="sxs-lookup"><span data-stu-id="f7218-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="f7218-122">Non è presente alcun blocco del conteggio, quindi esegue il wrapping in caso di overflow.</span><span class="sxs-lookup"><span data-stu-id="f7218-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="f7218-123">Lo stesso shader non è in grado di tentare di usare sia l' **\_ \_ allocazione** atomica di IMM che il **\_ \_ consumo atomico di IMM** nello stesso UAV.</span><span class="sxs-lookup"><span data-stu-id="f7218-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="f7218-124">Inoltre, la GPU non può consentire la combinazione di più chiamate shader per la combinazione di **IMM \_ Atomic \_ Alloc** e **IMM \_ Atomic \_ consume** nello stesso UAV.</span><span class="sxs-lookup"><span data-stu-id="f7218-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="f7218-125">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7218-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f7218-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="f7218-126">Vertex</span></span> | <span data-ttu-id="f7218-127">Hull</span><span class="sxs-lookup"><span data-stu-id="f7218-127">Hull</span></span> | <span data-ttu-id="f7218-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="f7218-128">Domain</span></span> | <span data-ttu-id="f7218-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="f7218-129">Geometry</span></span> | <span data-ttu-id="f7218-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="f7218-130">Pixel</span></span> | <span data-ttu-id="f7218-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f7218-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f7218-132">X</span><span class="sxs-lookup"><span data-stu-id="f7218-132">X</span></span>     | <span data-ttu-id="f7218-133">X</span><span class="sxs-lookup"><span data-stu-id="f7218-133">X</span></span>       |



 

<span data-ttu-id="f7218-134">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7218-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f7218-135">Vertice</span><span class="sxs-lookup"><span data-stu-id="f7218-135">Vertex</span></span> | <span data-ttu-id="f7218-136">Hull</span><span class="sxs-lookup"><span data-stu-id="f7218-136">Hull</span></span> | <span data-ttu-id="f7218-137">Dominio</span><span class="sxs-lookup"><span data-stu-id="f7218-137">Domain</span></span> | <span data-ttu-id="f7218-138">Geometria</span><span class="sxs-lookup"><span data-stu-id="f7218-138">Geometry</span></span> | <span data-ttu-id="f7218-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="f7218-139">Pixel</span></span> | <span data-ttu-id="f7218-140">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f7218-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f7218-141">X</span><span class="sxs-lookup"><span data-stu-id="f7218-141">X</span></span>      | <span data-ttu-id="f7218-142">X</span><span class="sxs-lookup"><span data-stu-id="f7218-142">X</span></span>    | <span data-ttu-id="f7218-143">X</span><span class="sxs-lookup"><span data-stu-id="f7218-143">X</span></span>      | <span data-ttu-id="f7218-144">X</span><span class="sxs-lookup"><span data-stu-id="f7218-144">X</span></span>        | <span data-ttu-id="f7218-145">X</span><span class="sxs-lookup"><span data-stu-id="f7218-145">X</span></span>     | <span data-ttu-id="f7218-146">X</span><span class="sxs-lookup"><span data-stu-id="f7218-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f7218-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f7218-147">Minimum Shader Model</span></span>

<span data-ttu-id="f7218-148">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7218-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f7218-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f7218-149">Shader Model</span></span>                                              | <span data-ttu-id="f7218-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="f7218-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f7218-151">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f7218-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f7218-152">sì</span><span class="sxs-lookup"><span data-stu-id="f7218-152">yes</span></span>       |
| [<span data-ttu-id="f7218-153">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f7218-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f7218-154">no</span><span class="sxs-lookup"><span data-stu-id="f7218-154">no</span></span>        |
| [<span data-ttu-id="f7218-155">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f7218-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f7218-156">no</span><span class="sxs-lookup"><span data-stu-id="f7218-156">no</span></span>        |
| [<span data-ttu-id="f7218-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7218-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f7218-158">no</span><span class="sxs-lookup"><span data-stu-id="f7218-158">no</span></span>        |
| [<span data-ttu-id="f7218-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7218-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f7218-160">no</span><span class="sxs-lookup"><span data-stu-id="f7218-160">no</span></span>        |
| [<span data-ttu-id="f7218-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7218-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f7218-162">no</span><span class="sxs-lookup"><span data-stu-id="f7218-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f7218-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7218-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7218-164">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7218-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





