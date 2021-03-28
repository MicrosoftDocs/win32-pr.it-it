---
title: store_structured (SM5-ASM)
description: Scrittura ad accesso casuale di componenti a 1-4 32 bit in una visualizzazione di accesso non ordinato (UAV) del buffer strutturato.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046078"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="779b0-103">archivio \_ strutturato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="779b0-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="779b0-104">Scrittura ad accesso casuale di componenti a 1-4 32 bit in una visualizzazione di accesso non ordinato (UAV) del buffer strutturato.</span><span class="sxs-lookup"><span data-stu-id="779b0-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="779b0-105">archivio \_ strutturato dst0 \[ . Write \_ mask \] , dstAddress \[ . Select \_ Component \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="779b0-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="779b0-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="779b0-106">Item</span></span>                                                                                                                       | <span data-ttu-id="779b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="779b0-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="779b0-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="779b0-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="779b0-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="779b0-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="779b0-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="779b0-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="779b0-111">\[nell' \] indirizzo in cui scrivere.</span><span class="sxs-lookup"><span data-stu-id="779b0-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="779b0-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="779b0-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="779b0-113">\[nell' \] indice della struttura da scrivere.</span><span class="sxs-lookup"><span data-stu-id="779b0-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="779b0-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="779b0-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="779b0-115">\[nei \] componenti da scrivere.</span><span class="sxs-lookup"><span data-stu-id="779b0-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="779b0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="779b0-116">Remarks</span></span>

<span data-ttu-id="779b0-117">Questa istruzione esegue 1-4 \* componenti a 32 bit del componente scritti da *src0* a *Dst0* all'indirizzo in *dstAddress* e *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="779b0-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="779b0-118">Nessuna conversione di formato.</span><span class="sxs-lookup"><span data-stu-id="779b0-118">No format conversion.</span></span>

<span data-ttu-id="779b0-119">*dst0* deve essere un UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="779b0-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="779b0-120">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="779b0-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="779b0-121">*dstAddress* specifica l'indice della struttura da scrivere.</span><span class="sxs-lookup"><span data-stu-id="779b0-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="779b0-122">Il percorso dei dati scritti equivale allo pseudocodice seguente che mostra l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="779b0-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="779b0-123">Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="779b0-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="779b0-124">Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.</span><span class="sxs-lookup"><span data-stu-id="779b0-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="779b0-125">*dst0* può avere solo una maschera di scrittura che è una delle seguenti:. x,. XY,. xyz,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="779b0-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="779b0-126">La maschera di scrittura determina il numero di componenti a 32 bit da scrivere senza gap.</span><span class="sxs-lookup"><span data-stu-id="779b0-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="779b0-127">Il superamento dei limiti in u \# cacitato da *dstAddress* significa che non viene scritto alcun elemento nella memoria fuori limite.</span><span class="sxs-lookup"><span data-stu-id="779b0-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="779b0-128">Se il *dstByteOffset*, incluso *dstWriteMask*, è ciò che causa l'accesso all'utente \# , l'intero contenuto del UAV diventa indefinito.</span><span class="sxs-lookup"><span data-stu-id="779b0-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="779b0-129">All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, l'intero contenuto di tutta la memoria condivisa diventerà indefinito.</span><span class="sxs-lookup"><span data-stu-id="779b0-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="779b0-130">*dstByteOffset* è un argomento separato da *dstAddress* perché si tratta in genere di un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="779b0-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="779b0-131">Questa separazione di parametri non è stata eseguita per gli atomici sulla memoria strutturata.</span><span class="sxs-lookup"><span data-stu-id="779b0-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="779b0-132">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="779b0-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="779b0-133">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="779b0-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="779b0-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="779b0-134">Vertex</span></span> | <span data-ttu-id="779b0-135">Hull</span><span class="sxs-lookup"><span data-stu-id="779b0-135">Hull</span></span> | <span data-ttu-id="779b0-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="779b0-136">Domain</span></span> | <span data-ttu-id="779b0-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="779b0-137">Geometry</span></span> | <span data-ttu-id="779b0-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="779b0-138">Pixel</span></span> | <span data-ttu-id="779b0-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="779b0-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="779b0-140">X</span><span class="sxs-lookup"><span data-stu-id="779b0-140">X</span></span>     | <span data-ttu-id="779b0-141">X</span><span class="sxs-lookup"><span data-stu-id="779b0-141">X</span></span>       |



 

<span data-ttu-id="779b0-142">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="779b0-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="779b0-143">Vertice</span><span class="sxs-lookup"><span data-stu-id="779b0-143">Vertex</span></span> | <span data-ttu-id="779b0-144">Hull</span><span class="sxs-lookup"><span data-stu-id="779b0-144">Hull</span></span> | <span data-ttu-id="779b0-145">Dominio</span><span class="sxs-lookup"><span data-stu-id="779b0-145">Domain</span></span> | <span data-ttu-id="779b0-146">Geometria</span><span class="sxs-lookup"><span data-stu-id="779b0-146">Geometry</span></span> | <span data-ttu-id="779b0-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="779b0-147">Pixel</span></span> | <span data-ttu-id="779b0-148">Calcolo</span><span class="sxs-lookup"><span data-stu-id="779b0-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="779b0-149">X</span><span class="sxs-lookup"><span data-stu-id="779b0-149">X</span></span>      | <span data-ttu-id="779b0-150">X</span><span class="sxs-lookup"><span data-stu-id="779b0-150">X</span></span>    | <span data-ttu-id="779b0-151">X</span><span class="sxs-lookup"><span data-stu-id="779b0-151">X</span></span>      | <span data-ttu-id="779b0-152">X</span><span class="sxs-lookup"><span data-stu-id="779b0-152">X</span></span>        | <span data-ttu-id="779b0-153">X</span><span class="sxs-lookup"><span data-stu-id="779b0-153">X</span></span>     | <span data-ttu-id="779b0-154">X</span><span class="sxs-lookup"><span data-stu-id="779b0-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="779b0-155">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="779b0-155">Minimum Shader Model</span></span>

<span data-ttu-id="779b0-156">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="779b0-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="779b0-157">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="779b0-157">Shader Model</span></span>                                              | <span data-ttu-id="779b0-158">Supportato</span><span class="sxs-lookup"><span data-stu-id="779b0-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="779b0-159">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="779b0-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="779b0-160">sì</span><span class="sxs-lookup"><span data-stu-id="779b0-160">yes</span></span>       |
| [<span data-ttu-id="779b0-161">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="779b0-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="779b0-162">no</span><span class="sxs-lookup"><span data-stu-id="779b0-162">no</span></span>        |
| [<span data-ttu-id="779b0-163">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="779b0-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="779b0-164">no</span><span class="sxs-lookup"><span data-stu-id="779b0-164">no</span></span>        |
| [<span data-ttu-id="779b0-165">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="779b0-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="779b0-166">no</span><span class="sxs-lookup"><span data-stu-id="779b0-166">no</span></span>        |
| [<span data-ttu-id="779b0-167">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="779b0-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="779b0-168">no</span><span class="sxs-lookup"><span data-stu-id="779b0-168">no</span></span>        |
| [<span data-ttu-id="779b0-169">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="779b0-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="779b0-170">no</span><span class="sxs-lookup"><span data-stu-id="779b0-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="779b0-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="779b0-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="779b0-172">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="779b0-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





