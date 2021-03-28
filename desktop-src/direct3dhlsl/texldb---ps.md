---
title: texldb-PS
description: Istruzione di caricamento trama distorta. Questa istruzione usa il quarto elemento (. a o. w) per inclinare il livello di dettaglio del campionamento della trama appena prima del campionamento.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117894"
---
# <a name="texldb---ps"></a><span data-ttu-id="4b14c-104">texldb-PS</span><span class="sxs-lookup"><span data-stu-id="4b14c-104">texldb - ps</span></span>

<span data-ttu-id="4b14c-105">Istruzione di caricamento trama distorta.</span><span class="sxs-lookup"><span data-stu-id="4b14c-105">Biased texture load instruction.</span></span> <span data-ttu-id="4b14c-106">Questa istruzione usa il quarto elemento (. a o. w) per inclinare il livello di dettaglio del campionamento della trama appena prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4b14c-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b14c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b14c-107">Syntax</span></span>



| <span data-ttu-id="4b14c-108">texldb DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4b14c-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="4b14c-109">Dove:</span><span class="sxs-lookup"><span data-stu-id="4b14c-109">Where:</span></span>

-   <span data-ttu-id="4b14c-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4b14c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="4b14c-111">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="4b14c-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="4b14c-112">Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="4b14c-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="4b14c-113">src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="4b14c-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="4b14c-114">Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="4b14c-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="4b14c-115">Per le restrizioni relative all'uso di texldb, vedere le istruzioni [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="4b14c-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="4b14c-116">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4b14c-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="4b14c-117">l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).</span><span class="sxs-lookup"><span data-stu-id="4b14c-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="4b14c-118">src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="4b14c-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="4b14c-119">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="4b14c-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="4b14c-120">Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT CAP non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama (texld, texldp, texldb, texldd) dipenda al massimo dal terzo ordine.</span><span class="sxs-lookup"><span data-stu-id="4b14c-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="4b14c-121">Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:</span><span class="sxs-lookup"><span data-stu-id="4b14c-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="4b14c-122">src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="4b14c-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="4b14c-123">l'ora legale è stata scritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4b14c-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="4b14c-124">Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine.</span><span class="sxs-lookup"><span data-stu-id="4b14c-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="4b14c-125">Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="4b14c-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="4b14c-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b14c-126">ps\_3\_0</span></span>

<span data-ttu-id="4b14c-127">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori.</span><span class="sxs-lookup"><span data-stu-id="4b14c-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="4b14c-128">Swizzle è consentito in src1 e, se applicato, i risultati della ricerca di trama sono pre-swizzled prima della scrittura nell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="4b14c-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b14c-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b14c-129">Remarks</span></span>



| <span data-ttu-id="4b14c-130">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="4b14c-130">Pixel shader versions</span></span> | <span data-ttu-id="4b14c-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="4b14c-131">1\_1</span></span> | <span data-ttu-id="4b14c-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="4b14c-132">1\_2</span></span> | <span data-ttu-id="4b14c-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4b14c-133">1\_3</span></span> | <span data-ttu-id="4b14c-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="4b14c-134">1\_4</span></span> | <span data-ttu-id="4b14c-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b14c-135">2\_0</span></span> | <span data-ttu-id="4b14c-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4b14c-136">2\_x</span></span> | <span data-ttu-id="4b14c-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b14c-137">2\_sw</span></span> | <span data-ttu-id="4b14c-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b14c-138">3\_0</span></span> | <span data-ttu-id="4b14c-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b14c-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4b14c-140">texldb</span><span class="sxs-lookup"><span data-stu-id="4b14c-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="4b14c-141">x</span><span class="sxs-lookup"><span data-stu-id="4b14c-141">x</span></span>    | <span data-ttu-id="4b14c-142">x</span><span class="sxs-lookup"><span data-stu-id="4b14c-142">x</span></span>    | <span data-ttu-id="4b14c-143">x</span><span class="sxs-lookup"><span data-stu-id="4b14c-143">x</span></span>     | <span data-ttu-id="4b14c-144">x</span><span class="sxs-lookup"><span data-stu-id="4b14c-144">x</span></span>    | <span data-ttu-id="4b14c-145">x</span><span class="sxs-lookup"><span data-stu-id="4b14c-145">x</span></span>     |



 

<span data-ttu-id="4b14c-146">texldb polarizza il livello di dettaglio mipmap, calcolato normalmente come parte del processo di esempio mediante il valore (con segno) in src0. w.</span><span class="sxs-lookup"><span data-stu-id="4b14c-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="4b14c-147">I valori di bias positivi comporteranno la selezione di mipmap più piccoli e viceversa.</span><span class="sxs-lookup"><span data-stu-id="4b14c-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="4b14c-148">Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, i valori di distorsione possono essere compresi nell'intervallo compreso tra \[ -3,0 e + 3,0 \] .</span><span class="sxs-lookup"><span data-stu-id="4b14c-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="4b14c-149">Per PS \_ 3 \_ 0, i valori di distorsione possono essere compresi nell'intervallo compreso tra \[ -16,0 e + 15,0 \] .</span><span class="sxs-lookup"><span data-stu-id="4b14c-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="4b14c-150">I valori di distorsione al di fuori di questi intervalli producono risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="4b14c-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="4b14c-151">Lo stato del campionatore D3DSAMP \_ MIPMAPLODBIAS viene comunque rispettato e la distorsione texldb viene aggiunta a questa, ma in base ai singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="4b14c-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="4b14c-152">Dopo il calcolo del livello di dettaglio distorta, D3DSAMP \_ MAXMIPLEVEL viene comunque rispettato e si verifica l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="4b14c-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="4b14c-153">Dopo texldb, il contenuto di src0 non è interessato (a meno che DST non sia lo stesso registro).</span><span class="sxs-lookup"><span data-stu-id="4b14c-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="4b14c-154">Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w.</span><span class="sxs-lookup"><span data-stu-id="4b14c-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="4b14c-155">I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4b14c-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="4b14c-156">Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XYW; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyzw.</span><span class="sxs-lookup"><span data-stu-id="4b14c-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="4b14c-157">Campionamento di una trama 2D con coordinate xyzw consentite (la coordinata. z viene ignorata).</span><span class="sxs-lookup"><span data-stu-id="4b14c-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="4b14c-158">Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="4b14c-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="4b14c-159">Le impostazioni predefinite dipendono dal formato di trama, come illustrato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="4b14c-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="4b14c-160">Formato trama</span><span class="sxs-lookup"><span data-stu-id="4b14c-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="4b14c-161">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="4b14c-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="4b14c-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT L8 \_ , D3DFMT L16 \_ , \_ \_ \_ D3DFMT R3G3B2, D3DFMT CxV8U8, D3DFMT L6V5U5</span><span class="sxs-lookup"><span data-stu-id="4b14c-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="4b14c-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="4b14c-163">A = 1.0</span></span>              |
| <span data-ttu-id="4b14c-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT G16R16 \_ , D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="4b14c-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="4b14c-165">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="4b14c-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="4b14c-166">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="4b14c-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="4b14c-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="4b14c-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="4b14c-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="4b14c-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="4b14c-169">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="4b14c-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="4b14c-170">Tutti i formati di profondità/stencil</span><span class="sxs-lookup"><span data-stu-id="4b14c-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="4b14c-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="4b14c-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4b14c-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b14c-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b14c-173">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="4b14c-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 