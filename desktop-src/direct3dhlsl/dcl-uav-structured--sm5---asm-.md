---
title: dcl_uav_structured (SM5-ASM)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234714"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="cc121-104">\_ \_ struttura di DCL UAV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cc121-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="cc121-105">Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader.</span><span class="sxs-lookup"><span data-stu-id="cc121-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="cc121-106">DCL \_ UAV \_ strutturato \[ \_ GLC \] dstUAV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="cc121-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="cc121-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc121-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="cc121-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc121-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="cc121-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="cc121-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="cc121-110">\[nel \] UAV.</span><span class="sxs-lookup"><span data-stu-id="cc121-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="cc121-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="cc121-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="cc121-112">\[nella \] dimensione della struttura in byte.</span><span class="sxs-lookup"><span data-stu-id="cc121-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc121-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc121-113">Remarks</span></span>

<span data-ttu-id="cc121-114">*dstUAV* è un \# registro u dichiarato come riferimento a un UnorderedAccessView di un buffer strutturato con lo stride specificato che deve essere associato allo slot UAV nell' \# API.</span><span class="sxs-lookup"><span data-stu-id="cc121-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="cc121-115">Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.</span><span class="sxs-lookup"><span data-stu-id="cc121-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="cc121-116">*structByteStride* è la dimensione della struttura in byte nel buffer dichiarato.</span><span class="sxs-lookup"><span data-stu-id="cc121-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="cc121-117">Il valore deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="cc121-117">This value must be greater than zero.</span></span> <span data-ttu-id="cc121-118">*structByteStride* è di tipo uint e deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="cc121-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="cc121-119">Le istruzioni che fanno riferimento a un'u strutturata \# accettano un indirizzo 2D, in cui il primo componente sceglie \[ struct \] e il secondo componente sceglie \[ offset all'interno dello struct, in byte allineati \] .</span><span class="sxs-lookup"><span data-stu-id="cc121-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="cc121-120">Il \_ flag GLC significa "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="cc121-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="cc121-121">L'assenza di \_ GLC significa che il UAV viene dichiarato solo come "gruppo coerente" nel compute shader o "coerente localmente" in una singola chiamata di pixel shader.</span><span class="sxs-lookup"><span data-stu-id="cc121-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="cc121-122">Il \_ flag OPC è il contatore per la conservazione degli ordini.</span><span class="sxs-lookup"><span data-stu-id="cc121-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="cc121-123">Indica che se un UAV è associato a uno slot \# (u \# ), è necessario che sia stato creato con il flag del contatore.</span><span class="sxs-lookup"><span data-stu-id="cc121-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="cc121-124">Ciò significa che le operazioni [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) nello shader consentono di modificare un contatore i cui valori possono essere usati nello shader come riferimento permanente a una posizione nell'UAV.</span><span class="sxs-lookup"><span data-stu-id="cc121-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="cc121-125">Non è possibile riordinare i dati dopo che lo shader è stato superato.</span><span class="sxs-lookup"><span data-stu-id="cc121-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="cc121-126">L'assenza del \_ flag OPC significa che se lo shader usa le istruzioni[IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) e un UAV è associato a slot \# (u), è necessario che sia stato creato con il flag Append, che fornisce un contatore che non garantisce che l'ordine venga mantenuto dopo la chiamata dello shader.</span><span class="sxs-lookup"><span data-stu-id="cc121-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="cc121-127">Se il \_ flag OPC è assente e lo shader non contiene le istruzioni [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) , è consentito creare un UAV associato a slot \# (u) con il flag del contatore (il contatore non verrà usato da questo shader), nessun flag (nessun contatore), ma non con il flag di Accodamento.</span><span class="sxs-lookup"><span data-stu-id="cc121-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="cc121-128">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano **DCL \_ TGSM \_ strutturate**, ma [non \_ TGSM DCL \_ RAW](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="cc121-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="cc121-129">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc121-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cc121-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="cc121-130">Vertex</span></span> | <span data-ttu-id="cc121-131">Hull</span><span class="sxs-lookup"><span data-stu-id="cc121-131">Hull</span></span> | <span data-ttu-id="cc121-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="cc121-132">Domain</span></span> | <span data-ttu-id="cc121-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="cc121-133">Geometry</span></span> | <span data-ttu-id="cc121-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="cc121-134">Pixel</span></span> | <span data-ttu-id="cc121-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cc121-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cc121-136">X</span><span class="sxs-lookup"><span data-stu-id="cc121-136">X</span></span>     | <span data-ttu-id="cc121-137">X</span><span class="sxs-lookup"><span data-stu-id="cc121-137">X</span></span>       |



 

<span data-ttu-id="cc121-138">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cc121-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="cc121-139">Vertice</span><span class="sxs-lookup"><span data-stu-id="cc121-139">Vertex</span></span> | <span data-ttu-id="cc121-140">Hull</span><span class="sxs-lookup"><span data-stu-id="cc121-140">Hull</span></span> | <span data-ttu-id="cc121-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="cc121-141">Domain</span></span> | <span data-ttu-id="cc121-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="cc121-142">Geometry</span></span> | <span data-ttu-id="cc121-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="cc121-143">Pixel</span></span> | <span data-ttu-id="cc121-144">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cc121-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cc121-145">X</span><span class="sxs-lookup"><span data-stu-id="cc121-145">X</span></span>      | <span data-ttu-id="cc121-146">X</span><span class="sxs-lookup"><span data-stu-id="cc121-146">X</span></span>    | <span data-ttu-id="cc121-147">X</span><span class="sxs-lookup"><span data-stu-id="cc121-147">X</span></span>      | <span data-ttu-id="cc121-148">X</span><span class="sxs-lookup"><span data-stu-id="cc121-148">X</span></span>        | <span data-ttu-id="cc121-149">X</span><span class="sxs-lookup"><span data-stu-id="cc121-149">X</span></span>     | <span data-ttu-id="cc121-150">X</span><span class="sxs-lookup"><span data-stu-id="cc121-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cc121-151">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="cc121-151">Minimum Shader Model</span></span>

<span data-ttu-id="cc121-152">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc121-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cc121-153">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="cc121-153">Shader Model</span></span>                                              | <span data-ttu-id="cc121-154">Supportato</span><span class="sxs-lookup"><span data-stu-id="cc121-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cc121-155">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="cc121-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cc121-156">sì</span><span class="sxs-lookup"><span data-stu-id="cc121-156">yes</span></span>       |
| [<span data-ttu-id="cc121-157">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="cc121-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cc121-158">no</span><span class="sxs-lookup"><span data-stu-id="cc121-158">no</span></span>        |
| [<span data-ttu-id="cc121-159">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="cc121-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cc121-160">no</span><span class="sxs-lookup"><span data-stu-id="cc121-160">no</span></span>        |
| [<span data-ttu-id="cc121-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc121-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cc121-162">no</span><span class="sxs-lookup"><span data-stu-id="cc121-162">no</span></span>        |
| [<span data-ttu-id="cc121-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc121-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cc121-164">no</span><span class="sxs-lookup"><span data-stu-id="cc121-164">no</span></span>        |
| [<span data-ttu-id="cc121-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc121-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cc121-166">no</span><span class="sxs-lookup"><span data-stu-id="cc121-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="cc121-167">Questa istruzione è supportata in cs \_ 4 \_ 0 e cs \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="cc121-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc121-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc121-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc121-169">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc121-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





