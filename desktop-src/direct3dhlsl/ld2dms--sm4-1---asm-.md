---
title: ld2dms (SM 4.1-ASM)
description: Legge singoli campioni da trame multicampionate bidimensionali.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117205"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="66150-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="66150-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="66150-104">Legge singoli campioni da trame multicampionate bidimensionali.</span><span class="sxs-lookup"><span data-stu-id="66150-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="66150-105">ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , sampleIndex (operando scalare)</span><span class="sxs-lookup"><span data-stu-id="66150-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="66150-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="66150-106">Item</span></span>                                                                                                               | <span data-ttu-id="66150-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66150-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66150-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="66150-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="66150-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="66150-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="66150-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="66150-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="66150-111">\[nelle \] coordinate di trama necessarie per eseguire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="66150-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="66150-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="66150-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="66150-113">\[in \] un registro di trama (t \# ) che deve essere stato dichiarato che identifica la trama o il buffer da cui recuperare</span><span class="sxs-lookup"><span data-stu-id="66150-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="66150-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="66150-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="66150-115">\[in \] Idendifies gli esempi per leggere da *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="66150-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="66150-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="66150-116">Remarks</span></span>

<span data-ttu-id="66150-117">Questa istruzione è un'alternativa semplificata all'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="66150-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="66150-118">Recupera i dati dalla trama specificata senza filtrare, ad esempio il campionamento dei punti, usando il valore integer *srcAddress* e *sampleIndex* fornito.</span><span class="sxs-lookup"><span data-stu-id="66150-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="66150-119">*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio sotto forma di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="66150-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="66150-120">Se *srcAddress* non è compreso nell'intervallo \[ 0... ( \# Texels in Dimension-1) \] , **ld2dms** restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="66150-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="66150-121">*sampleIndex* non deve essere un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="66150-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="66150-122">Il conteggio multisample non deve essere specificato nella risorsa di trama e funziona con le visualizzazioni depth o stencil.</span><span class="sxs-lookup"><span data-stu-id="66150-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="66150-123">Un'applicazione che desidera un controllo più flessibile sul comportamento degli indirizzi non compresi nell'intervallo deve invece utilizzare l'istruzione di **esempio** , in quanto rispetta il comportamento di ritorno a capo/mirroring/morsetto/bordo definito come stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="66150-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="66150-124">*srcAddress. b* (post-swizzle) viene ignorato per Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="66150-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="66150-125">Se il valore non è compreso nell'intervallo degli indici di matrice disponibili \[ 0... ( dimensione della matrice-1) \] , quindi **ld2dms** restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="66150-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="66150-126">Per le matrici Texture2D, *srcAddress. b* (post-swizzle) fornisce l'indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="66150-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="66150-127">Oherwise ha lo stesso comportamento di Texture2D.</span><span class="sxs-lookup"><span data-stu-id="66150-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="66150-128">*srcAddress. a* (post-swizzle) viene sempre ignorato.</span><span class="sxs-lookup"><span data-stu-id="66150-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="66150-129">Il compilatore HLSL non restituirà mai alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="66150-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="66150-130">*srcResource* è un registro di trama (t \# ) che deve essere stato dichiarato (22.3.11), identificando la trama da cui recuperare.</span><span class="sxs-lookup"><span data-stu-id="66150-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="66150-131">Il recupero da t \# a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="66150-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="66150-132">Offset indirizzo</span><span class="sxs-lookup"><span data-stu-id="66150-132">Address Offset</span></span>

<span data-ttu-id="66150-133">Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per il **ld2dms** devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato.</span><span class="sxs-lookup"><span data-stu-id="66150-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="66150-134">I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="66150-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="66150-135">Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="66150-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="66150-136">Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="66150-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="66150-137">I componenti *\_ aoffimmi v, w* vengono ignorati per Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="66150-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="66150-138">Il componente *\_ aoffimmi w* viene ignorato per Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="66150-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="66150-139">Poiché le coordinate di trama per **ld2dms** sono interi senza segno, se l'offset fa sì che l'indirizzo vada al di sotto di zero, verrà eseguito il wrapping a un indirizzo di grandi dimensioni e il risultato sarà un accesso fuori limite, che come **LD** restituisce 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti</span><span class="sxs-lookup"><span data-stu-id="66150-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="66150-140">Numero di esempio</span><span class="sxs-lookup"><span data-stu-id="66150-140">Sample Number</span></span>

<span data-ttu-id="66150-141">**ld2dms** è disponibile per l'uso in qualsiasi risorsa.</span><span class="sxs-lookup"><span data-stu-id="66150-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="66150-142">**ld2dms** funziona in modo identico a **LD** tranne che nelle risorse multsample 2D, usando l'operando *sampleIndex* aggiuntivo (basato su 0) per identificare l'esempio da leggere dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="66150-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="66150-143">Il risultato della specifica di un *sampleIndex* che supera il numero di campioni nella risorsa non è definito, ma non può restituire dati all'esterno dello spazio degli indirizzi del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66150-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="66150-144">Controllo tipo restituito</span><span class="sxs-lookup"><span data-stu-id="66150-144">Return Type Control</span></span>

<span data-ttu-id="66150-145">Il formato dei dati restituito da **ld2dms** al registro di destinazione viene determinato in modo analogo a quanto descritto per l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="66150-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="66150-146">Si basa sul formato associato al parametro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="66150-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="66150-147">Come per l'istruzione di **esempio** , i valori restituiti per **ld2dms** sono 4 vettori con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato.</span><span class="sxs-lookup"><span data-stu-id="66150-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="66150-148">Il swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dal caricamento della trama, dopo il quale. mask su *dest* determina quali componenti in *dest* vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="66150-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="66150-149">Quando un valore float a 32 bit viene letto da **ld2dms** in un registro a 32 bit, i bit non vengono modificati; ovvero i valori denormali rimangono denormalizzati.</span><span class="sxs-lookup"><span data-stu-id="66150-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="66150-150">Questo è diverso dall'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="66150-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="66150-151">Dettagli vari</span><span class="sxs-lookup"><span data-stu-id="66150-151">Miscellaneous Details</span></span>

<span data-ttu-id="66150-152">Poiché non esiste alcun filtro associato a questa istruzione, concetti come la distorsione del LOD non si applicano.</span><span class="sxs-lookup"><span data-stu-id="66150-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="66150-153">Di conseguenza non è presente alcun parametro del *campionatore \#* .</span><span class="sxs-lookup"><span data-stu-id="66150-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="66150-154">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="66150-154">Restrictions</span></span>

-   <span data-ttu-id="66150-155">*srcResource* deve essere un \# Registro t e non TextureCube, Texture1D o Texture1DArray.</span><span class="sxs-lookup"><span data-stu-id="66150-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="66150-156">*srcResource* non può essere un ConstantBuffer, che non può essere associato a \# registri t.</span><span class="sxs-lookup"><span data-stu-id="66150-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="66150-157">L'indirizzamento relativo in *srcResource* non è consentito.</span><span class="sxs-lookup"><span data-stu-id="66150-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="66150-158">*srcAddress* e *sampleIndex* devono essere un registro temp (r \# /x \# ), Constant (CB \# ) o input (v \# ).</span><span class="sxs-lookup"><span data-stu-id="66150-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="66150-159">il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="66150-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="66150-160">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="66150-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="66150-161">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="66150-161">Vertex Shader</span></span> | <span data-ttu-id="66150-162">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="66150-162">Geometry Shader</span></span> | <span data-ttu-id="66150-163">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="66150-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="66150-164">x</span><span class="sxs-lookup"><span data-stu-id="66150-164">x</span></span>             | <span data-ttu-id="66150-165">x</span><span class="sxs-lookup"><span data-stu-id="66150-165">x</span></span>               | <span data-ttu-id="66150-166">x</span><span class="sxs-lookup"><span data-stu-id="66150-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="66150-167">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="66150-167">Minimum Shader Model</span></span>

<span data-ttu-id="66150-168">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="66150-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="66150-169">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="66150-169">Shader Model</span></span>                                              | <span data-ttu-id="66150-170">Supportato</span><span class="sxs-lookup"><span data-stu-id="66150-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="66150-171">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="66150-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="66150-172">sì</span><span class="sxs-lookup"><span data-stu-id="66150-172">yes</span></span>       |
| [<span data-ttu-id="66150-173">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="66150-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="66150-174">sì</span><span class="sxs-lookup"><span data-stu-id="66150-174">yes</span></span>       |
| [<span data-ttu-id="66150-175">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="66150-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="66150-176">no</span><span class="sxs-lookup"><span data-stu-id="66150-176">no</span></span>        |
| [<span data-ttu-id="66150-177">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66150-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="66150-178">no</span><span class="sxs-lookup"><span data-stu-id="66150-178">no</span></span>        |
| [<span data-ttu-id="66150-179">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66150-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="66150-180">no</span><span class="sxs-lookup"><span data-stu-id="66150-180">no</span></span>        |
| [<span data-ttu-id="66150-181">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66150-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="66150-182">no</span><span class="sxs-lookup"><span data-stu-id="66150-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="66150-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66150-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66150-184">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66150-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





