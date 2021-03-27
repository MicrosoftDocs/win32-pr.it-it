---
title: ld_structured (SM5-ASM)
description: Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer strutturato.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398260"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="702cb-103">LD \_ strutturato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="702cb-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="702cb-104">Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer strutturato.</span><span class="sxs-lookup"><span data-stu-id="702cb-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="702cb-105">: LD \_ strutturato dst0 \[ . mask \] , srcAddress \[ . Select \_ Component \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="702cb-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="702cb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="702cb-106">Item</span></span>                                                                                                                       | <span data-ttu-id="702cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="702cb-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="702cb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="702cb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="702cb-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="702cb-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="702cb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="702cb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="702cb-111">\[in \] specifica l'indice della struttura da leggere.</span><span class="sxs-lookup"><span data-stu-id="702cb-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="702cb-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="702cb-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="702cb-113">\[in \] specifica l'offset di byte nella struttura da cui iniziare la lettura.</span><span class="sxs-lookup"><span data-stu-id="702cb-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="702cb-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="702cb-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="702cb-115">Il buffer da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="702cb-115">The buffer to read from.</span></span> <span data-ttu-id="702cb-116">Questo parametro deve essere un SRV (t \# ), UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="702cb-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="702cb-117">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="702cb-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="702cb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="702cb-118">Remarks</span></span>

<span data-ttu-id="702cb-119">I dati letti dalla struttura sono equivalenti al seguente pseudocodice: dove abbiamo l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="702cb-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="702cb-120">Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="702cb-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="702cb-121">Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.</span><span class="sxs-lookup"><span data-stu-id="702cb-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="702cb-122">Il superamento dei limiti per u \# /t \# di un determinato componente a 32 bit restituisce 0 per quel componente, tranne nel caso in cui *srcByteOffset*, oltre a swizzle sia il risultato che impedisce l'accesso all'utente \# /t \# , il valore restituito per tutti i componenti non è definito.</span><span class="sxs-lookup"><span data-stu-id="702cb-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="702cb-123">All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, restituiscono un risultato non definito.</span><span class="sxs-lookup"><span data-stu-id="702cb-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="702cb-124">*srcByteOffset* è un argomento separato da *srcAddress* perché si tratta in genere di un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="702cb-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="702cb-125">Questa separazione di parametri non è stata eseguita per gli atomici sulla memoria strutturata.</span><span class="sxs-lookup"><span data-stu-id="702cb-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="702cb-126">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="702cb-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="702cb-127">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="702cb-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="702cb-128">Vertice</span><span class="sxs-lookup"><span data-stu-id="702cb-128">Vertex</span></span> | <span data-ttu-id="702cb-129">Hull</span><span class="sxs-lookup"><span data-stu-id="702cb-129">Hull</span></span> | <span data-ttu-id="702cb-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="702cb-130">Domain</span></span> | <span data-ttu-id="702cb-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="702cb-131">Geometry</span></span> | <span data-ttu-id="702cb-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="702cb-132">Pixel</span></span> | <span data-ttu-id="702cb-133">Calcolo</span><span class="sxs-lookup"><span data-stu-id="702cb-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="702cb-134">X</span><span class="sxs-lookup"><span data-stu-id="702cb-134">X</span></span>      | <span data-ttu-id="702cb-135">X</span><span class="sxs-lookup"><span data-stu-id="702cb-135">X</span></span>    | <span data-ttu-id="702cb-136">X</span><span class="sxs-lookup"><span data-stu-id="702cb-136">X</span></span>      | <span data-ttu-id="702cb-137">X</span><span class="sxs-lookup"><span data-stu-id="702cb-137">X</span></span>        | <span data-ttu-id="702cb-138">X</span><span class="sxs-lookup"><span data-stu-id="702cb-138">X</span></span>     | <span data-ttu-id="702cb-139">X</span><span class="sxs-lookup"><span data-stu-id="702cb-139">X</span></span>       |



 

<span data-ttu-id="702cb-140">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per UAV per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="702cb-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="702cb-141">Vertice</span><span class="sxs-lookup"><span data-stu-id="702cb-141">Vertex</span></span> | <span data-ttu-id="702cb-142">Hull</span><span class="sxs-lookup"><span data-stu-id="702cb-142">Hull</span></span> | <span data-ttu-id="702cb-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="702cb-143">Domain</span></span> | <span data-ttu-id="702cb-144">Geometria</span><span class="sxs-lookup"><span data-stu-id="702cb-144">Geometry</span></span> | <span data-ttu-id="702cb-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="702cb-145">Pixel</span></span> | <span data-ttu-id="702cb-146">Calcolo</span><span class="sxs-lookup"><span data-stu-id="702cb-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="702cb-147">X</span><span class="sxs-lookup"><span data-stu-id="702cb-147">X</span></span>      | <span data-ttu-id="702cb-148">X</span><span class="sxs-lookup"><span data-stu-id="702cb-148">X</span></span>    | <span data-ttu-id="702cb-149">X</span><span class="sxs-lookup"><span data-stu-id="702cb-149">X</span></span>      | <span data-ttu-id="702cb-150">X</span><span class="sxs-lookup"><span data-stu-id="702cb-150">X</span></span>        | <span data-ttu-id="702cb-151">X</span><span class="sxs-lookup"><span data-stu-id="702cb-151">X</span></span>     | <span data-ttu-id="702cb-152">X</span><span class="sxs-lookup"><span data-stu-id="702cb-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="702cb-153">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="702cb-153">Minimum Shader Model</span></span>

<span data-ttu-id="702cb-154">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="702cb-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="702cb-155">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="702cb-155">Shader Model</span></span>                                              | <span data-ttu-id="702cb-156">Supportato</span><span class="sxs-lookup"><span data-stu-id="702cb-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="702cb-157">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="702cb-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="702cb-158">sì</span><span class="sxs-lookup"><span data-stu-id="702cb-158">yes</span></span>       |
| [<span data-ttu-id="702cb-159">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="702cb-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="702cb-160">no</span><span class="sxs-lookup"><span data-stu-id="702cb-160">no</span></span>        |
| [<span data-ttu-id="702cb-161">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="702cb-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="702cb-162">no</span><span class="sxs-lookup"><span data-stu-id="702cb-162">no</span></span>        |
| [<span data-ttu-id="702cb-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="702cb-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="702cb-164">no</span><span class="sxs-lookup"><span data-stu-id="702cb-164">no</span></span>        |
| [<span data-ttu-id="702cb-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="702cb-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="702cb-166">no</span><span class="sxs-lookup"><span data-stu-id="702cb-166">no</span></span>        |
| [<span data-ttu-id="702cb-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="702cb-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="702cb-168">no</span><span class="sxs-lookup"><span data-stu-id="702cb-168">no</span></span>        |



 

<span data-ttu-id="702cb-169">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="702cb-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="702cb-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="702cb-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="702cb-171">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="702cb-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





