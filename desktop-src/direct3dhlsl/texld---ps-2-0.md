---
title: texld-ps_2_0 e su
description: Campionare una trama in un particolare campionatore, usando le coordinate di trama fornite. Questa istruzione è diversa dall'istruzione texld-PS \_ 1 \_ 4 usata in pixel shader versione 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516887"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="77d6c-104">texld-PS \_ 2 \_ 0 e su</span><span class="sxs-lookup"><span data-stu-id="77d6c-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="77d6c-105">Campionare una trama in un particolare campionatore, usando le coordinate di trama fornite.</span><span class="sxs-lookup"><span data-stu-id="77d6c-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="77d6c-106">Questa istruzione è diversa dall'istruzione [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) usata in pixel shader versione 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="77d6c-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d6c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77d6c-107">Syntax</span></span>



| <span data-ttu-id="77d6c-108">texld DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="77d6c-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="77d6c-109">Dove:</span><span class="sxs-lookup"><span data-stu-id="77d6c-109">Where:</span></span>

-   <span data-ttu-id="77d6c-110">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77d6c-110">dst is a destination register.</span></span>
-   <span data-ttu-id="77d6c-111">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="77d6c-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="77d6c-112">src1 identifica il [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , dove specifica il \# numero di campionamento di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="77d6c-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="77d6c-113">Il campionatore è associato a una trama e a uno stato del campionatore definito da [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="77d6c-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="77d6c-114">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="77d6c-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="77d6c-115">l'ora legale deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) ed è consentita solo la maschera xyzw (maschera predefinita).</span><span class="sxs-lookup"><span data-stu-id="77d6c-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="77d6c-116">src0 deve essere un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="77d6c-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="77d6c-117">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatore o Swizzle.</span><span class="sxs-lookup"><span data-stu-id="77d6c-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="77d6c-118">Se il \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT non è impostato (in D3DPSHADERCAPS2 \_ 0), è possibile che una determinata istruzione di trama ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) dipenda al massimo dal terzo ordine.</span><span class="sxs-lookup"><span data-stu-id="77d6c-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="77d6c-119">Un'istruzione di trama dipendente dal primo ordine è un'istruzione di trama in cui:</span><span class="sxs-lookup"><span data-stu-id="77d6c-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="77d6c-120">src0 è un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="77d6c-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="77d6c-121">l'ora legale è stata scritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="77d6c-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="77d6c-122">Un'istruzione di trama dipendente di secondo ordine è definita come un'istruzione di trama che legge o scrive in un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) il cui contenuto, prima di eseguire l'istruzione di trama, dipende (forse indirettamente) dal risultato di un'istruzione di trama dipendente dal primo ordine.</span><span class="sxs-lookup"><span data-stu-id="77d6c-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="77d6c-123">Un'<sup>istruzione di trama</sup>dipendente dall'ordine (n) deriva da un'istruzione di trama dell'ordine (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="77d6c-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="77d6c-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77d6c-124">ps\_3\_0</span></span>

<span data-ttu-id="77d6c-125">src1 deve essere un [campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , senza modificatori.</span><span class="sxs-lookup"><span data-stu-id="77d6c-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="77d6c-126">Swizzle è consentito in src0 o src1.</span><span class="sxs-lookup"><span data-stu-id="77d6c-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="77d6c-127">Swizzle viene applicato alla trama coordintates prima della ricerca della trama.</span><span class="sxs-lookup"><span data-stu-id="77d6c-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d6c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="77d6c-128">Remarks</span></span>

<span data-ttu-id="77d6c-129">Questa istruzione è supportata nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="77d6c-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="77d6c-130">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="77d6c-130">Pixel shader versions</span></span> | <span data-ttu-id="77d6c-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="77d6c-131">1\_1</span></span> | <span data-ttu-id="77d6c-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="77d6c-132">1\_2</span></span> | <span data-ttu-id="77d6c-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77d6c-133">1\_3</span></span> | <span data-ttu-id="77d6c-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="77d6c-134">1\_4</span></span> | <span data-ttu-id="77d6c-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77d6c-135">2\_0</span></span> | <span data-ttu-id="77d6c-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="77d6c-136">2\_x</span></span> | <span data-ttu-id="77d6c-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77d6c-137">2\_sw</span></span> | <span data-ttu-id="77d6c-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77d6c-138">3\_0</span></span> | <span data-ttu-id="77d6c-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77d6c-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="77d6c-140">texld</span><span class="sxs-lookup"><span data-stu-id="77d6c-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="77d6c-141">x</span><span class="sxs-lookup"><span data-stu-id="77d6c-141">x</span></span>    | <span data-ttu-id="77d6c-142">x</span><span class="sxs-lookup"><span data-stu-id="77d6c-142">x</span></span>    | <span data-ttu-id="77d6c-143">x</span><span class="sxs-lookup"><span data-stu-id="77d6c-143">x</span></span>     | <span data-ttu-id="77d6c-144">x</span><span class="sxs-lookup"><span data-stu-id="77d6c-144">x</span></span>    | <span data-ttu-id="77d6c-145">x</span><span class="sxs-lookup"><span data-stu-id="77d6c-145">x</span></span>     |



 

<span data-ttu-id="77d6c-146">Il numero di coordinate necessarie per l'esecuzione dell'esempio di trama da parte di src0 dipende dalla modalità con cui è stato dichiarato src1, più dal componente. w.</span><span class="sxs-lookup"><span data-stu-id="77d6c-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="77d6c-147">I tipi di campionatore sono dichiarati con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="77d6c-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="77d6c-148">Se src1 viene dichiarato come campionatore 2D, src0 deve contenere le coordinate. XY; Se src1 viene dichiarato come Sampler del cubo o campionatore del volume, src0 deve contenere le coordinate. xyz.</span><span class="sxs-lookup"><span data-stu-id="77d6c-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="77d6c-149">Il campionamento di una trama con meno dimensioni rispetto a quelli presenti nella coordinata di trama è consentito perché i componenti delle coordinate di trama aggiuntivi vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="77d6c-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="77d6c-150">Se la trama di origine contiene meno di quattro componenti, i valori predefiniti vengono inseriti nei componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="77d6c-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="77d6c-151">Le impostazioni predefinite dipendono dal formato di trama, come illustrato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="77d6c-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="77d6c-152">Formato trama</span><span class="sxs-lookup"><span data-stu-id="77d6c-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="77d6c-153">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="77d6c-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="77d6c-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT L8 \_ , D3DFMT L16 \_ , \_ \_ \_ D3DFMT R3G3B2, D3DFMT CxV8U8, D3DFMT L6V5U5</span><span class="sxs-lookup"><span data-stu-id="77d6c-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="77d6c-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="77d6c-155">A = 1.0</span></span>              |
| <span data-ttu-id="77d6c-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT G16R16 \_ , D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="77d6c-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="77d6c-157">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="77d6c-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="77d6c-158">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="77d6c-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="77d6c-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="77d6c-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="77d6c-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="77d6c-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="77d6c-161">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="77d6c-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="77d6c-162">Tutti i formati di profondità/stencil</span><span class="sxs-lookup"><span data-stu-id="77d6c-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="77d6c-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="77d6c-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="77d6c-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77d6c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77d6c-165">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="77d6c-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 