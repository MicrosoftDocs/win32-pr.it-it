---
title: store_raw (SM5-ASM)
description: Scrittura ad accesso casuale di componenti a 32 bit 1-4 nella memoria di tipo.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398286"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="dac05-103">archivio \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="dac05-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="dac05-104">Scrittura ad accesso casuale di componenti a 32 bit 1-4 nella memoria di tipo.</span><span class="sxs-lookup"><span data-stu-id="dac05-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="dac05-105">archiviare una \_ maschera dst0. Write non elaborata \[ \_ \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dac05-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dac05-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dac05-106">Item</span></span>                                                                                                                       | <span data-ttu-id="dac05-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dac05-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="dac05-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="dac05-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="dac05-109">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="dac05-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="dac05-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="dac05-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="dac05-111">\[nell' \] offset.</span><span class="sxs-lookup"><span data-stu-id="dac05-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="dac05-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dac05-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="dac05-113">\[nei \] componenti da scrivere.</span><span class="sxs-lookup"><span data-stu-id="dac05-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dac05-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dac05-114">Remarks</span></span>

<span data-ttu-id="dac05-115">Questa istruzione esegue i componenti a 1-4 bit del componente \* 32 scritti da *src0* a *dst0* in corrispondenza dell'offset in *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="dac05-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="dac05-116">Nessuna conversione di formato.</span><span class="sxs-lookup"><span data-stu-id="dac05-116">There is no format conversion.</span></span>

<span data-ttu-id="dac05-117">il valore di *dst0* deve essere un UAV (u \# ) o nel compute shader. può anche essere una memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="dac05-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="dac05-118">*dstByteOffset* specifica il valore di base a 32 bit in memoria per una finestra di 4 valori sequenziali a 32 bit in cui è possibile scrivere i dati, a seconda di swizzle e maschera su altri parametri.</span><span class="sxs-lookup"><span data-stu-id="dac05-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="dac05-119">Il percorso dei dati scritti equivale al seguente pseudocodice che mostra l'indirizzo, il puntatore al contenuto del buffer e i dati archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="dac05-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="dac05-120">Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="dac05-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="dac05-121">*dst0* può avere solo una maschera di scrittura che è una delle seguenti:. x,. XY,. xyz,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="dac05-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="dac05-122">La maschera di scrittura determina il numero di componenti a 32 bit da scrivere senza gap.</span><span class="sxs-lookup"><span data-stu-id="dac05-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="dac05-123">All'esterno dei limiti di indirizzamento su u \# significa che non viene scritto nulla nella memoria fuori limite; qualsiasi parte che si trova nei limiti viene scritta correttamente.</span><span class="sxs-lookup"><span data-stu-id="dac05-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="dac05-124">All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, l'intero contenuto di tutta la memoria condivisa diventerà indefinito.</span><span class="sxs-lookup"><span data-stu-id="dac05-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="dac05-125">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV.</span><span class="sxs-lookup"><span data-stu-id="dac05-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="dac05-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac05-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dac05-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="dac05-127">Vertex</span></span> | <span data-ttu-id="dac05-128">Hull</span><span class="sxs-lookup"><span data-stu-id="dac05-128">Hull</span></span> | <span data-ttu-id="dac05-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="dac05-129">Domain</span></span> | <span data-ttu-id="dac05-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="dac05-130">Geometry</span></span> | <span data-ttu-id="dac05-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="dac05-131">Pixel</span></span> | <span data-ttu-id="dac05-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dac05-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dac05-133">X</span><span class="sxs-lookup"><span data-stu-id="dac05-133">X</span></span>     | <span data-ttu-id="dac05-134">X</span><span class="sxs-lookup"><span data-stu-id="dac05-134">X</span></span>       |



 

<span data-ttu-id="dac05-135">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dac05-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="dac05-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="dac05-136">Vertex</span></span> | <span data-ttu-id="dac05-137">Hull</span><span class="sxs-lookup"><span data-stu-id="dac05-137">Hull</span></span> | <span data-ttu-id="dac05-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="dac05-138">Domain</span></span> | <span data-ttu-id="dac05-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="dac05-139">Geometry</span></span> | <span data-ttu-id="dac05-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="dac05-140">Pixel</span></span> | <span data-ttu-id="dac05-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dac05-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dac05-142">X</span><span class="sxs-lookup"><span data-stu-id="dac05-142">X</span></span>      | <span data-ttu-id="dac05-143">X</span><span class="sxs-lookup"><span data-stu-id="dac05-143">X</span></span>    | <span data-ttu-id="dac05-144">X</span><span class="sxs-lookup"><span data-stu-id="dac05-144">X</span></span>      | <span data-ttu-id="dac05-145">X</span><span class="sxs-lookup"><span data-stu-id="dac05-145">X</span></span>        | <span data-ttu-id="dac05-146">X</span><span class="sxs-lookup"><span data-stu-id="dac05-146">X</span></span>     | <span data-ttu-id="dac05-147">X</span><span class="sxs-lookup"><span data-stu-id="dac05-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dac05-148">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="dac05-148">Minimum Shader Model</span></span>

<span data-ttu-id="dac05-149">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac05-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="dac05-150">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="dac05-150">Shader Model</span></span>                                              | <span data-ttu-id="dac05-151">Supportato</span><span class="sxs-lookup"><span data-stu-id="dac05-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dac05-152">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dac05-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dac05-153">sì</span><span class="sxs-lookup"><span data-stu-id="dac05-153">yes</span></span>       |
| [<span data-ttu-id="dac05-154">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="dac05-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dac05-155">no</span><span class="sxs-lookup"><span data-stu-id="dac05-155">no</span></span>        |
| [<span data-ttu-id="dac05-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="dac05-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dac05-157">no</span><span class="sxs-lookup"><span data-stu-id="dac05-157">no</span></span>        |
| [<span data-ttu-id="dac05-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac05-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dac05-159">no</span><span class="sxs-lookup"><span data-stu-id="dac05-159">no</span></span>        |
| [<span data-ttu-id="dac05-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac05-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dac05-161">no</span><span class="sxs-lookup"><span data-stu-id="dac05-161">no</span></span>        |
| [<span data-ttu-id="dac05-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac05-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dac05-163">no</span><span class="sxs-lookup"><span data-stu-id="dac05-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dac05-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dac05-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac05-165">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac05-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





