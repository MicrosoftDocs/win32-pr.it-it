---
title: ld_raw (SM5-ASM)
description: Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer non elaborato.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976399"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="6d55b-103">LD \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6d55b-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="6d55b-104">Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer non elaborato.</span><span class="sxs-lookup"><span data-stu-id="6d55b-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="6d55b-105">LD \_ RAW dst0 \[ . mask \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6d55b-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="6d55b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6d55b-106">Item</span></span>                                                                                                                       | <span data-ttu-id="6d55b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d55b-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6d55b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="6d55b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="6d55b-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6d55b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6d55b-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="6d55b-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="6d55b-111">\[in \] specifica l'offset da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="6d55b-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="6d55b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6d55b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="6d55b-113">\[nel \] componente da leggere.</span><span class="sxs-lookup"><span data-stu-id="6d55b-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6d55b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d55b-114">Remarks</span></span>

<span data-ttu-id="6d55b-115">*src0* deve essere:</span><span class="sxs-lookup"><span data-stu-id="6d55b-115">*src0* must be:</span></span>

-   <span data-ttu-id="6d55b-116">Qualsiasi fase dello shader: SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="6d55b-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="6d55b-117">Compute shader o pixel shader: UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="6d55b-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="6d55b-118">Compute Shader: memoria condivisa del gruppo di thread (g \# )</span><span class="sxs-lookup"><span data-stu-id="6d55b-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="6d55b-119">*srcByteOffset* specifica il valore di base a 32 bit in memoria per una finestra di 4 valori sequenziali a 32 bit in cui è possibile leggere i dati, a seconda di swizzle e maschera su altri parametri.</span><span class="sxs-lookup"><span data-stu-id="6d55b-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="6d55b-120">I dati letti dal buffer non elaborato sono equivalenti al seguente pseudocodice: dove abbiamo l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="6d55b-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="6d55b-121">Il superamento dei limiti per u \# /t \# di un determinato componente a 32 bit restituisce 0 per quel componente.</span><span class="sxs-lookup"><span data-stu-id="6d55b-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="6d55b-122">All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, restituiscono un risultato non definito.</span><span class="sxs-lookup"><span data-stu-id="6d55b-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="6d55b-123">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="6d55b-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="6d55b-124">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d55b-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6d55b-125">Vertice</span><span class="sxs-lookup"><span data-stu-id="6d55b-125">Vertex</span></span> | <span data-ttu-id="6d55b-126">Hull</span><span class="sxs-lookup"><span data-stu-id="6d55b-126">Hull</span></span> | <span data-ttu-id="6d55b-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="6d55b-127">Domain</span></span> | <span data-ttu-id="6d55b-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="6d55b-128">Geometry</span></span> | <span data-ttu-id="6d55b-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d55b-129">Pixel</span></span> | <span data-ttu-id="6d55b-130">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6d55b-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d55b-131">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-131">X</span></span>      | <span data-ttu-id="6d55b-132">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-132">X</span></span>    | <span data-ttu-id="6d55b-133">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-133">X</span></span>      | <span data-ttu-id="6d55b-134">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-134">X</span></span>        | <span data-ttu-id="6d55b-135">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-135">X</span></span>     | <span data-ttu-id="6d55b-136">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-136">X</span></span>       |



 

<span data-ttu-id="6d55b-137">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per UAV per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d55b-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="6d55b-138">Vertice</span><span class="sxs-lookup"><span data-stu-id="6d55b-138">Vertex</span></span> | <span data-ttu-id="6d55b-139">Hull</span><span class="sxs-lookup"><span data-stu-id="6d55b-139">Hull</span></span> | <span data-ttu-id="6d55b-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="6d55b-140">Domain</span></span> | <span data-ttu-id="6d55b-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="6d55b-141">Geometry</span></span> | <span data-ttu-id="6d55b-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d55b-142">Pixel</span></span> | <span data-ttu-id="6d55b-143">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6d55b-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d55b-144">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-144">X</span></span>      | <span data-ttu-id="6d55b-145">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-145">X</span></span>    | <span data-ttu-id="6d55b-146">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-146">X</span></span>      | <span data-ttu-id="6d55b-147">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-147">X</span></span>        | <span data-ttu-id="6d55b-148">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-148">X</span></span>     | <span data-ttu-id="6d55b-149">X</span><span class="sxs-lookup"><span data-stu-id="6d55b-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6d55b-150">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6d55b-150">Minimum Shader Model</span></span>

<span data-ttu-id="6d55b-151">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d55b-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6d55b-152">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6d55b-152">Shader Model</span></span>                                              | <span data-ttu-id="6d55b-153">Supportato</span><span class="sxs-lookup"><span data-stu-id="6d55b-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6d55b-154">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6d55b-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6d55b-155">sì</span><span class="sxs-lookup"><span data-stu-id="6d55b-155">yes</span></span>       |
| [<span data-ttu-id="6d55b-156">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="6d55b-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6d55b-157">no</span><span class="sxs-lookup"><span data-stu-id="6d55b-157">no</span></span>        |
| [<span data-ttu-id="6d55b-158">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="6d55b-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6d55b-159">no</span><span class="sxs-lookup"><span data-stu-id="6d55b-159">no</span></span>        |
| [<span data-ttu-id="6d55b-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d55b-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6d55b-161">no</span><span class="sxs-lookup"><span data-stu-id="6d55b-161">no</span></span>        |
| [<span data-ttu-id="6d55b-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d55b-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6d55b-163">no</span><span class="sxs-lookup"><span data-stu-id="6d55b-163">no</span></span>        |
| [<span data-ttu-id="6d55b-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d55b-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6d55b-165">no</span><span class="sxs-lookup"><span data-stu-id="6d55b-165">no</span></span>        |



 

<span data-ttu-id="6d55b-166">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="6d55b-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d55b-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d55b-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d55b-168">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d55b-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





