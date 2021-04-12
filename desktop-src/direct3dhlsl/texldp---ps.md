---
title: texldp-PS
description: Istruzione di caricamento trama proiettata. Questa istruzione divide la coordinata di trama di input in base al quarto elemento (. a o. w) appena prima del campionamento.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339151"
---
# <a name="texldp---ps"></a><span data-ttu-id="3f8ff-104">texldp-PS</span><span class="sxs-lookup"><span data-stu-id="3f8ff-104">texldp - ps</span></span>

<span data-ttu-id="3f8ff-105">Istruzione di caricamento trama proiettata.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-105">Projected texture load instruction.</span></span> <span data-ttu-id="3f8ff-106">Questa istruzione divide la coordinata di trama di input in base al quarto elemento (. a o. w) appena prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f8ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f8ff-107">Syntax</span></span>



| <span data-ttu-id="3f8ff-108">texldp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3f8ff-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="3f8ff-109">dove</span><span class="sxs-lookup"><span data-stu-id="3f8ff-109">where</span></span>

-   <span data-ttu-id="3f8ff-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-110">dst is the destination register.</span></span>
-   <span data-ttu-id="3f8ff-111">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="3f8ff-112">Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="3f8ff-113">src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="3f8ff-114">Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="3f8ff-115">Per il set di restrizioni quando si usa texldp, vedere [texld](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f8ff-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f8ff-116">Remarks</span></span>

<span data-ttu-id="3f8ff-117">texldp esegue la proiezione sulle coordinate lette da src0 prima di eseguire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="3f8ff-118">Ogni coordinata di trama è divisa per src0. w, quindi la trama viene campionata.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="3f8ff-119">Al termine dell'esecuzione di texldp, il contenuto di src0 non è interessato (a meno che DST non sia lo stesso registro).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="3f8ff-120">Un'alternativa all'uso di texldp consiste nell'eseguire manualmente la divisione della proiezione nello shader.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="3f8ff-121">Tuttavia, l'esecuzione della divisione nel codice dello shader è in genere più lenta rispetto a quando viene eseguita dall'istruzione texldp, evitando così una matematica aggiuntiva, quando possibile.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="3f8ff-122">Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="3f8ff-123">I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="3f8ff-124">Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XYW; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyzw.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="3f8ff-125">Campionamento di una trama 2D con coordinate xyzw consentite (la coordinata. z viene ignorata).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="3f8ff-126">Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="3f8ff-127">Le impostazioni predefinite dipendono dal formato di trama, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="3f8ff-128">Formato trama</span><span class="sxs-lookup"><span data-stu-id="3f8ff-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="3f8ff-129">Valori predefiniti per i componenti mancanti</span><span class="sxs-lookup"><span data-stu-id="3f8ff-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="3f8ff-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT L8 \_ , D3DFMT L16 \_ , \_ \_ \_ D3DFMT R3G3B2, D3DFMT CxV8U8, D3DFMT L6V5U5</span><span class="sxs-lookup"><span data-stu-id="3f8ff-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="3f8ff-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-131">A = 1.0</span></span>                               |
| <span data-ttu-id="3f8ff-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT G16R16 \_ , D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="3f8ff-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="3f8ff-133">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="3f8ff-134">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="3f8ff-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="3f8ff-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="3f8ff-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="3f8ff-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="3f8ff-137">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="3f8ff-138">Tutti i formati di profondità/stencil</span><span class="sxs-lookup"><span data-stu-id="3f8ff-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="3f8ff-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="3f8ff-140">Questa istruzione è supportata nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3f8ff-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="3f8ff-141">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3f8ff-141">Pixel shader versions</span></span> | <span data-ttu-id="3f8ff-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="3f8ff-142">1\_1</span></span> | <span data-ttu-id="3f8ff-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="3f8ff-143">1\_2</span></span> | <span data-ttu-id="3f8ff-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f8ff-144">1\_3</span></span> | <span data-ttu-id="3f8ff-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="3f8ff-145">1\_4</span></span> | <span data-ttu-id="3f8ff-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-146">2\_0</span></span> | <span data-ttu-id="3f8ff-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-147">2\_x</span></span> | <span data-ttu-id="3f8ff-148">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f8ff-148">2\_sw</span></span> | <span data-ttu-id="3f8ff-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-149">3\_0</span></span> | <span data-ttu-id="3f8ff-150">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f8ff-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3f8ff-151">texldp</span><span class="sxs-lookup"><span data-stu-id="3f8ff-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="3f8ff-152">x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-152">x</span></span>    | <span data-ttu-id="3f8ff-153">x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-153">x</span></span>    | <span data-ttu-id="3f8ff-154">x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-154">x</span></span>     | <span data-ttu-id="3f8ff-155">x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-155">x</span></span>    | <span data-ttu-id="3f8ff-156">x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="3f8ff-157">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f8ff-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="3f8ff-158">l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).</span><span class="sxs-lookup"><span data-stu-id="3f8ff-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="3f8ff-159">src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="3f8ff-160">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="3f8ff-161">Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) dipenda al massimo dal terzo ordine.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="3f8ff-162">Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:</span><span class="sxs-lookup"><span data-stu-id="3f8ff-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="3f8ff-163">src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="3f8ff-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="3f8ff-164">l'ora legale è stata scritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="3f8ff-165">Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="3f8ff-166">Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="3f8ff-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="3f8ff-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f8ff-167">ps\_3\_0</span></span>

<span data-ttu-id="3f8ff-168">Per PS \_ 3 \_ 0, src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="3f8ff-169">Swizzle è consentito in src1 e, se applicato, i risultati della ricerca di trama sono pre-swizzled prima della scrittura nell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="3f8ff-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f8ff-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f8ff-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f8ff-171">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3f8ff-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 