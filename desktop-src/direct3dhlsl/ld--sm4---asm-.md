---
title: LD (SM4-ASM)
description: Recupera i dati dal buffer o dalla trama specificati senza filtrare, ad esempio il campionamento dei punti, usando l'indirizzo integer fornito. I dati di origine possono provenire da qualsiasi tipo di risorsa, diverso da TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335540"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="32a6d-104">LD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="32a6d-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="32a6d-105">Recupera i dati dal buffer o dalla trama specificati senza filtrare, ad esempio il campionamento dei punti, usando l'indirizzo integer fornito.</span><span class="sxs-lookup"><span data-stu-id="32a6d-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="32a6d-106">I dati di origine possono provenire da qualsiasi tipo di risorsa, diverso da TextureCube.</span><span class="sxs-lookup"><span data-stu-id="32a6d-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="32a6d-107">LD \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="32a6d-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="32a6d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="32a6d-108">Item</span></span>                                                                                                               | <span data-ttu-id="32a6d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32a6d-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a6d-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="32a6d-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="32a6d-111">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="32a6d-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="32a6d-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="32a6d-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="32a6d-113">\[nelle \] coordinate di trama necessarie per eseguire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="32a6d-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="32a6d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="32a6d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="32a6d-115">\[in \] un registro di trama (t \# ) che deve essere stato dichiarato che identifica la trama o il buffer da cui recuperare.</span><span class="sxs-lookup"><span data-stu-id="32a6d-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32a6d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="32a6d-116">Remarks</span></span>

<span data-ttu-id="32a6d-117">Questa istruzione è un'alternativa semplificata all'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="32a6d-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="32a6d-118">A differenza di **esempio**, **LD** è anche in grado di recuperare i dati dai buffer.</span><span class="sxs-lookup"><span data-stu-id="32a6d-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="32a6d-119">**LD** è anche in grado di recuperare da risorse di più campioni (solo pixel shader).</span><span class="sxs-lookup"><span data-stu-id="32a6d-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="32a6d-120">*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio sotto forma di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="32a6d-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="32a6d-121">Se *srcAddress* non è compreso nell'intervallo \[ 0... ( \# Texels nella dimensione 1) \] , viene richiamato il comportamento out-of-Bounds, dove **LD** restituisce 0 in tutti i componenti non mancanti del formato di *srcResource* e il valore predefinito per i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="32a6d-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="32a6d-122">Un'applicazione che desidera un controllo più flessibile sul comportamento degli indirizzi non compresi nell'intervallo deve invece utilizzare l'istruzione di **esempio** , in quanto rispetta il comportamento di ritorno a capo/mirroring/morsetto/bordo definito come stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="32a6d-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="32a6d-123">*srcAddress. a* (POS-swizzle) fornisce sempre un livello Unsigned Integer mipmap.</span><span class="sxs-lookup"><span data-stu-id="32a6d-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="32a6d-124">Se il valore non è compreso nell'intervallo \[ 0... ( Num mipLevels in Resource-1) \] , viene richiamato il comportamento out-of-Bounds.</span><span class="sxs-lookup"><span data-stu-id="32a6d-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="32a6d-125">Se la risorsa è un buffer, che non può avere mipmap, *srcAddress. a* viene ignorato</span><span class="sxs-lookup"><span data-stu-id="32a6d-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="32a6d-126">*srcAddress. GB* (POS-swizzle) viene ignorato per i buffer e texture1D (non matrice).</span><span class="sxs-lookup"><span data-stu-id="32a6d-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="32a6d-127">*srcAddress. b* (POS-swizzle) viene ignorato per le matrici Texture1D e texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="32a6d-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="32a6d-128">Per le matrici texture1D, *srcAddress. g* (POS-swizzle) fornisce l'indice della matrice come Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="32a6d-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="32a6d-129">Se il valore non è compreso nell'intervallo degli indici di matrice disponibili \[ 0... ( dimensione della matrice-1) \] , viene richiamato il comportamento fuori limite.</span><span class="sxs-lookup"><span data-stu-id="32a6d-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="32a6d-130">Per le matrici texture2D, *srcAddress. b* (POS-swizzle) fornisce l'indice della matrice, in caso contrario con la stessa semantica di texture1D.</span><span class="sxs-lookup"><span data-stu-id="32a6d-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="32a6d-131">Il recupero da *t \#* a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="32a6d-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="32a6d-132">Offset indirizzo</span><span class="sxs-lookup"><span data-stu-id="32a6d-132">Address Offset</span></span>

<span data-ttu-id="32a6d-133">Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per il **LD** devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato.</span><span class="sxs-lookup"><span data-stu-id="32a6d-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="32a6d-134">I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="32a6d-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="32a6d-135">Questo modificatore è definito solo per texture1D/2D/3D, incluse le matrici e non per i buffer.</span><span class="sxs-lookup"><span data-stu-id="32a6d-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="32a6d-136">Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel, rispetto alla miplevel a cui si accede tramite **LD**.</span><span class="sxs-lookup"><span data-stu-id="32a6d-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="32a6d-137">Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="32a6d-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="32a6d-138">I componenti *\_ aoffimmi v, w* vengono ignorati per texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="32a6d-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="32a6d-139">Il componente *\_ aoffimmi w* viene ignorato per texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="32a6d-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="32a6d-140">Poiché le coordinate di trama per **LD** sono interi senza segno, se l'offset fa sì che l'indirizzo vada al di sotto di zero, verrà eseguito il wrapping a un indirizzo di grandi dimensioni e il risultato sarà un accesso fuori limite.</span><span class="sxs-lookup"><span data-stu-id="32a6d-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="32a6d-141">Controllo tipo restituito</span><span class="sxs-lookup"><span data-stu-id="32a6d-141">Return Type Control</span></span>

<span data-ttu-id="32a6d-142">Il formato dati restituito da **LD** al registro di destinazione viene determinato in modo analogo a quanto descritto per l'istruzione di **esempio** . si basa sul formato associato al parametro *srcResource* (*t \#*).</span><span class="sxs-lookup"><span data-stu-id="32a6d-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="32a6d-143">Come per l'istruzione di **esempio** , i valori restituiti per **LD** sono 4 vettori con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato.</span><span class="sxs-lookup"><span data-stu-id="32a6d-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="32a6d-144">Il swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dal caricamento della trama, dopo il quale. mask su *dest* determina quali componenti in *dest* vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="32a6d-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="32a6d-145">Quando un valore float a 32 bit viene letto da *LD* in un registro a 32 bit, i bit non vengono modificati; ovvero i valori denormali rimangono denormalizzati.</span><span class="sxs-lookup"><span data-stu-id="32a6d-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="32a6d-146">Questo è diverso dall'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="32a6d-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="32a6d-147">Dettagli vari</span><span class="sxs-lookup"><span data-stu-id="32a6d-147">Miscellaneous Details</span></span>

<span data-ttu-id="32a6d-148">Poiché non esiste alcun filtro associato all'istruzione **LD** , concetti come la distorsione di LOD non si applicano a **LD**.</span><span class="sxs-lookup"><span data-stu-id="32a6d-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="32a6d-149">Di conseguenza non è presente *alcun \# parametro del* campionatore.</span><span class="sxs-lookup"><span data-stu-id="32a6d-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="32a6d-150">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="32a6d-150">Restrictions</span></span>

-   <span data-ttu-id="32a6d-151">*srcResource* deve essere un \# Registro t e non un TextureCube.</span><span class="sxs-lookup"><span data-stu-id="32a6d-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="32a6d-152">*srcResource* non può essere un ConstantBuffer né associato a \# registri t.</span><span class="sxs-lookup"><span data-stu-id="32a6d-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="32a6d-153">L'indirizzamento relativo in *srcResource* non è consentito.</span><span class="sxs-lookup"><span data-stu-id="32a6d-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="32a6d-154">*srcAddress* deve essere un registro temp (r \# /x \# ), Constant (CB \# ) o input (v \# ).</span><span class="sxs-lookup"><span data-stu-id="32a6d-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="32a6d-155">il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="32a6d-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="32a6d-156">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="32a6d-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="32a6d-157">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="32a6d-157">Vertex Shader</span></span> | <span data-ttu-id="32a6d-158">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="32a6d-158">Geometry Shader</span></span> | <span data-ttu-id="32a6d-159">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="32a6d-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="32a6d-160">x</span><span class="sxs-lookup"><span data-stu-id="32a6d-160">x</span></span>             | <span data-ttu-id="32a6d-161">x</span><span class="sxs-lookup"><span data-stu-id="32a6d-161">x</span></span>               | <span data-ttu-id="32a6d-162">x</span><span class="sxs-lookup"><span data-stu-id="32a6d-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="32a6d-163">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="32a6d-163">Minimum Shader Model</span></span>

<span data-ttu-id="32a6d-164">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="32a6d-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="32a6d-165">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="32a6d-165">Shader Model</span></span>                                              | <span data-ttu-id="32a6d-166">Supportato</span><span class="sxs-lookup"><span data-stu-id="32a6d-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="32a6d-167">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="32a6d-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="32a6d-168">sì</span><span class="sxs-lookup"><span data-stu-id="32a6d-168">yes</span></span>       |
| [<span data-ttu-id="32a6d-169">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="32a6d-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="32a6d-170">sì</span><span class="sxs-lookup"><span data-stu-id="32a6d-170">yes</span></span>       |
| [<span data-ttu-id="32a6d-171">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="32a6d-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="32a6d-172">sì</span><span class="sxs-lookup"><span data-stu-id="32a6d-172">yes</span></span>       |
| [<span data-ttu-id="32a6d-173">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32a6d-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="32a6d-174">no</span><span class="sxs-lookup"><span data-stu-id="32a6d-174">no</span></span>        |
| [<span data-ttu-id="32a6d-175">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32a6d-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="32a6d-176">no</span><span class="sxs-lookup"><span data-stu-id="32a6d-176">no</span></span>        |
| [<span data-ttu-id="32a6d-177">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32a6d-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="32a6d-178">no</span><span class="sxs-lookup"><span data-stu-id="32a6d-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="32a6d-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32a6d-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32a6d-180">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32a6d-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





