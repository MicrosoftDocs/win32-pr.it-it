---
title: esempio (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | esempio (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969193"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="9e30d-104">esempio (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9e30d-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="9e30d-105">Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.</span><span class="sxs-lookup"><span data-stu-id="9e30d-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="9e30d-106">aoffimmi di esempio \[ \_ (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="9e30d-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9e30d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9e30d-107">Item</span></span>                                                                                                               | <span data-ttu-id="9e30d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e30d-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e30d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9e30d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9e30d-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9e30d-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="9e30d-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="9e30d-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="9e30d-112">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="9e30d-113">Per ulteriori informazioni, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="9e30d-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="9e30d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="9e30d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9e30d-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-115">\[in\] A texture register.</span></span> <span data-ttu-id="9e30d-116">Per ulteriori informazioni, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="9e30d-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="9e30d-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="9e30d-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="9e30d-118">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="9e30d-118">\[in\] A sampler register.</span></span> <span data-ttu-id="9e30d-119">Per ulteriori informazioni, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="9e30d-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="9e30d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e30d-120">Remarks</span></span>

<span data-ttu-id="9e30d-121">I dati di origine possono provenire da qualsiasi tipo di risorsa, ad eccezione dei buffer.</span><span class="sxs-lookup"><span data-stu-id="9e30d-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="9e30d-122">*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio, come valori a virgola mobile che fanno riferimento allo spazio normalizzato nella trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="9e30d-123">Le modalità di wrapping degli indirizzi (wrap, mirror, Clamp/Border e così via) vengono applicate per le coordinate di trama \[ al di fuori di 0... 1 \] intervallo, tratto dagli Stati del campionatore \# e applicate dopo l'applicazione di un offset di indirizzo alle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="9e30d-124">*srcResource* è un registro di trama (t \# ).</span><span class="sxs-lookup"><span data-stu-id="9e30d-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="9e30d-125">Si tratta semplicemente di un segnaposto per una trama, incluso il tipo di dati restituito della risorsa da campionare.</span><span class="sxs-lookup"><span data-stu-id="9e30d-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="9e30d-126">Tutte queste informazioni sono dichiarate nel preambolo dello shader.</span><span class="sxs-lookup"><span data-stu-id="9e30d-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="9e30d-127">La risorsa effettiva da campionare è associata allo shader all'esterno dello slot \# (per t \# ).</span><span class="sxs-lookup"><span data-stu-id="9e30d-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="9e30d-128">*srcSampler* è uno o più registri del campionatore.</span><span class="sxs-lookup"><span data-stu-id="9e30d-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="9e30d-129">Si tratta semplicemente di un segnaposto per una raccolta di controlli di filtro, ad esempio Point vs. Linear, mapping MIP e i controlli di wrapping degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="9e30d-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="9e30d-130">Il set di informazioni necessarie per l'hardware per eseguire il campionamento è suddiviso in due parti ortogonali.</span><span class="sxs-lookup"><span data-stu-id="9e30d-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="9e30d-131">In primo luogo, il registro di trama fornisce informazioni sul tipo di dati di origine, ad esempio informazioni sulla presenza o meno di dati SRGB nella trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="9e30d-132">Fa anche riferimento alla memoria effettivamente campionata.</span><span class="sxs-lookup"><span data-stu-id="9e30d-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="9e30d-133">In secondo luogo, il registro campionatore definisce la modalità di filtro da applicare.</span><span class="sxs-lookup"><span data-stu-id="9e30d-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="9e30d-134">Risorse di matrice</span><span class="sxs-lookup"><span data-stu-id="9e30d-134">Array Resources</span></span>

<span data-ttu-id="9e30d-135">Per le matrici Texture1D, il componente g *srcAddress* (POS-swizzle) seleziona la sezione della matrice da cui recuperare.</span><span class="sxs-lookup"><span data-stu-id="9e30d-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="9e30d-136">Questo viene sempre considerato come un valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard e viene applicato un arrotondamento al valore più vicino, seguito da un morsetto all'intervallo di BufferArray disponibile.</span><span class="sxs-lookup"><span data-stu-id="9e30d-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="9e30d-137">Per le matrici Texture2D, il componente *srcAddress* b (POS-swizzle) seleziona la sezione della matrice da cui eseguire il recupero; in caso contrario, usando la stessa semantica descritta per le matrici Texture1D.</span><span class="sxs-lookup"><span data-stu-id="9e30d-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="9e30d-138">Offset indirizzo</span><span class="sxs-lookup"><span data-stu-id="9e30d-138">Address Offset</span></span>

<span data-ttu-id="9e30d-139">Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per l'esempio devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato.</span><span class="sxs-lookup"><span data-stu-id="9e30d-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="9e30d-140">I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="9e30d-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="9e30d-141">Questo modificatore viene definito per tutte le risorse, incluse le matrici Texture1D/2D e Texture3D, ma non è definito per TextureCube.</span><span class="sxs-lookup"><span data-stu-id="9e30d-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="9e30d-142">L'hardware può trarre vantaggio dalla conoscenza immediata che un attraversamento di un footprint di Texel su una posizione comune viene eseguito da un set di istruzioni di esempio.</span><span class="sxs-lookup"><span data-stu-id="9e30d-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="9e30d-143">Questo può essere trasmesso usando \_ aoffimmi (u, v, w).</span><span class="sxs-lookup"><span data-stu-id="9e30d-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="9e30d-144">Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel, rispetto a ogni miplevel a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="9e30d-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="9e30d-145">Quindi, anche se le coordinate di trama vengono fornite come valori float normalizzati, l'offset applica un offset integer dello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="9e30d-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="9e30d-146">Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="9e30d-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="9e30d-147">\_i componenti aoffimmi v, w vengono ignorati per Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="9e30d-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="9e30d-148">\_il componente aoffimmi w viene ignorato per Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="9e30d-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="9e30d-149">Le modalità di wrapping degli indirizzi (wrap, mirror, Clamp/Border e così via) dagli Stati del campionatore \# vengono applicate dopo che è stato applicato un offset di indirizzo alle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="9e30d-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="9e30d-150">Controllo tipo restituito</span><span class="sxs-lookup"><span data-stu-id="9e30d-150">Return Type Control</span></span>

<span data-ttu-id="9e30d-151">Il formato di dati restituito dall'esempio al registro di destinazione è determinato dal formato di risorsa ( \_ formato DXGI \* ) associato al parametro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="9e30d-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="9e30d-152">Se, ad esempio, l'oggetto t specificato \# è stato associato a una risorsa nel formato DXGI \_ Format \_ A8B8G8R8 \_ UNORM \_ sRGB, l'operazione di campionamento convertirà texel campionati da gamma 2,0 a 1,0, applica filtro e il risultato verrà scritto nel registro di destinazione come valori a virgola mobile nell'intervallo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="9e30d-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="9e30d-153">I valori restituiti sono 4 vettori (con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato).</span><span class="sxs-lookup"><span data-stu-id="9e30d-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="9e30d-154">Swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dall'esempio di trama/filtro, dopo il quale. mask on *dest* determina i componenti in *dest* che vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="9e30d-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="9e30d-155">Quando l' **esempio** legge un valore float a 32 bit in un registro a 32 bit, con il campionamento dei punti (nessun filtro), è possibile che non vengano scaricati i valori denormalizzati, ma in caso contrario i numeri non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="9e30d-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="9e30d-156">Se l'incertezza con i valori denormalizzati del campionamento dei punti è un problema per un'applicazione, usare l'istruzione [LD](ld--sm4---asm-.md) , che garantisce che i valori float a 32 bit siano letti senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="9e30d-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="9e30d-157">Calcolo LOD</span><span class="sxs-lookup"><span data-stu-id="9e30d-157">LOD Calculation</span></span>

<span data-ttu-id="9e30d-158">Per informazioni dettagliate su come vengono calcolati i derivati nel processo di determinazione di LOD per il filtro, vedere [derivare \_ RTX](deriv-rtx--sm4---asm-.md) e [derivare \_ valore](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="9e30d-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="9e30d-159">L'istruzione di **esempio** calcola in modo implicito i derivati sulle coordinate di trama utilizzando la stessa definizione utilizzata dalle istruzioni di **derivazione** dello shader.</span><span class="sxs-lookup"><span data-stu-id="9e30d-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="9e30d-160">Questa operazione non si applica alle istruzioni [Sample \_ l](sample-l--sm4---asm-.md) o [ \_ d Sample](sample-d--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="9e30d-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="9e30d-161">Per queste istruzioni, i LOD o i derivati vengono forniti direttamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e30d-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="9e30d-162">Per l'istruzione di **esempio** , le implementazioni possono scegliere di condividere lo stesso calcolo di LOD in tutti i 4 pixel in un timbro 2x2 (ma non in un'area più grande) o di eseguire calcoli LOD per pixel.</span><span class="sxs-lookup"><span data-stu-id="9e30d-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="9e30d-163">Dettagli vari</span><span class="sxs-lookup"><span data-stu-id="9e30d-163">Miscellaneous Details</span></span>

<span data-ttu-id="9e30d-164">Per il buffer & Texture1D, i componenti *srcAddress* . GBA (POS-swizzle) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="9e30d-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="9e30d-165">Per le matrici Texture1D, i componenti *srcAddress* . BA (POS-swizzle) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="9e30d-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="9e30d-166">Per Texture2Ds, *srcAddress* . un componente (POS-swizzle) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9e30d-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="9e30d-167">Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="9e30d-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="9e30d-168">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="9e30d-168">Restrictions</span></span>

-   <span data-ttu-id="9e30d-169">*srcResource* deve essere un \# Registro t.</span><span class="sxs-lookup"><span data-stu-id="9e30d-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="9e30d-170">*srcResource* non può essere un ConstantBuffer, che non può essere associato a \# registri t.</span><span class="sxs-lookup"><span data-stu-id="9e30d-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="9e30d-171">*srcSampler* deve essere un \# registro s.</span><span class="sxs-lookup"><span data-stu-id="9e30d-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="9e30d-172">L'indirizzamento relativo in *srcResource* o *srcSampler* non è consentito.</span><span class="sxs-lookup"><span data-stu-id="9e30d-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="9e30d-173">*srcAddress* deve essere un registro temp (r \# /X \# ), constantBuffer (CB \# ), input (v \# ) o un valore immediato.</span><span class="sxs-lookup"><span data-stu-id="9e30d-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="9e30d-174">il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="9e30d-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="9e30d-175">\_aoffimmi (u, v, w) non è consentito per TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="9e30d-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="9e30d-176">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e30d-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9e30d-177">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9e30d-177">Vertex Shader</span></span> | <span data-ttu-id="9e30d-178">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9e30d-178">Geometry Shader</span></span> | <span data-ttu-id="9e30d-179">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9e30d-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="9e30d-180">x</span><span class="sxs-lookup"><span data-stu-id="9e30d-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9e30d-181">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9e30d-181">Minimum Shader Model</span></span>

<span data-ttu-id="9e30d-182">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e30d-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9e30d-183">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9e30d-183">Shader Model</span></span>                                              | <span data-ttu-id="9e30d-184">Supportato</span><span class="sxs-lookup"><span data-stu-id="9e30d-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9e30d-185">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9e30d-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9e30d-186">sì</span><span class="sxs-lookup"><span data-stu-id="9e30d-186">yes</span></span>       |
| [<span data-ttu-id="9e30d-187">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9e30d-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9e30d-188">sì</span><span class="sxs-lookup"><span data-stu-id="9e30d-188">yes</span></span>       |
| [<span data-ttu-id="9e30d-189">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9e30d-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9e30d-190">sì</span><span class="sxs-lookup"><span data-stu-id="9e30d-190">yes</span></span>       |
| [<span data-ttu-id="9e30d-191">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e30d-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9e30d-192">no</span><span class="sxs-lookup"><span data-stu-id="9e30d-192">no</span></span>        |
| [<span data-ttu-id="9e30d-193">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e30d-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9e30d-194">no</span><span class="sxs-lookup"><span data-stu-id="9e30d-194">no</span></span>        |
| [<span data-ttu-id="9e30d-195">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e30d-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9e30d-196">no</span><span class="sxs-lookup"><span data-stu-id="9e30d-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9e30d-197">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e30d-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e30d-198">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e30d-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





