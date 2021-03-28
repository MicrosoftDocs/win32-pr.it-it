---
title: ResInfo (SM4-ASM)
description: Eseguire una query sulle dimensioni di una determinata risorsa di input.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398227"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="15035-103">ResInfo (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="15035-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="15035-104">Eseguire una query sulle dimensioni di una determinata risorsa di input.</span><span class="sxs-lookup"><span data-stu-id="15035-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="15035-105">ResInfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="15035-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="15035-106">\_rcpFloat \] dest \[ . mask \] , srcMipLevel. Select \_ Component, srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="15035-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="15035-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="15035-107">Item</span></span>                                                                                                               | <span data-ttu-id="15035-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15035-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="15035-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="15035-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="15035-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="15035-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="15035-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span><span class="sxs-lookup"><span data-stu-id="15035-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="15035-112">\[nel \] livello MIP.</span><span class="sxs-lookup"><span data-stu-id="15035-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="15035-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="15035-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="15035-114">\[in \] una \# \# trama di input t o u per la quale vengono eseguite query sulle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="15035-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="15035-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="15035-115">Remarks</span></span>

<span data-ttu-id="15035-116">*srcMipLevel* viene letto come Unsigned Integer scalare, quindi è necessario un selettore di componenti singolo per il registro di origine, se non è un valore scalare immediato.</span><span class="sxs-lookup"><span data-stu-id="15035-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="15035-117">*dest* riceve \[ la larghezza, l'altezza, la profondità o la dimensione della matrice, Total-MIP-Count \] , selezionato dalla maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="15035-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="15035-118">I valori di larghezza, altezza e profondità restituiti sono per il livello MIP selezionato dal parametro *srcMipLevel* e sono in numero di Texel, indipendentemente dalle dimensioni dei dati Texel.</span><span class="sxs-lookup"><span data-stu-id="15035-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="15035-119">Per le risorse multisample (texture2D \[ array \] MS \# ), le dimensioni e l'altezza vengono restituite anche nei Texel, non negli esempi.</span><span class="sxs-lookup"><span data-stu-id="15035-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="15035-120">Il numero totale MIP restituito in *dest. w* non è influenzato dal parametro *srcMipLevel* .</span><span class="sxs-lookup"><span data-stu-id="15035-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="15035-121">Per UAV (u \# ), il numero di livelli MIP è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="15035-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="15035-122">Tutti gli aspetti di questa istruzione sono basati sulle caratteristiche della visualizzazione risorse associate a t \# /u \# , non alla risorsa di base sottostante.</span><span class="sxs-lookup"><span data-stu-id="15035-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="15035-123">I valori restituiti sono tutti a virgola mobile, a meno che non \_ venga usato il modificatore uint, nel qual caso i valori restituiti sono tutti numeri interi.</span><span class="sxs-lookup"><span data-stu-id="15035-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="15035-124">Se \_ viene usato il modificatore rcpFloat, tutti i valori restituiti sono a virgola mobile e la larghezza, l'altezza e la profondità vengono restituiti come reciproci (1.0 f/Width, 1.0 f/Height, 1.0 f/depth), incluso inf se Width/Height/depth sono 0 dal comportamento *srcMipLevel* out-of-range.</span><span class="sxs-lookup"><span data-stu-id="15035-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="15035-125">Il \_ modificatore rcpFloat si applica solo ai valori di larghezza, altezza e profondità restituiti e non si applica ai valori impostati su 0 e pertanto non restituiti e non si applica anche alle dimensioni della matrice restituite.</span><span class="sxs-lookup"><span data-stu-id="15035-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="15035-126">Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="15035-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="15035-127">Se *srcResource* è un Texture1D, la larghezza viene restituita in *dest. x* e *dest. YZ* viene impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="15035-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="15035-128">Se *srcResource* è un Texture1DArray, la larghezza viene restituita in *dest. x*, la dimensione della matrice viene restituita in *dest. y* e *dest. z* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="15035-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="15035-129">Se *srcResource* è un Texture2D, la larghezza e l'altezza vengono restituite in *dest. XY* e *dest. z* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="15035-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="15035-130">Se *srcResource* è un Texture2DArray, la larghezza e l'altezza vengono restituite in *dest. XY* e la dimensione della matrice viene restituita in *dest. z*.</span><span class="sxs-lookup"><span data-stu-id="15035-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="15035-131">Se *srcResource* è un Texture3D, viene restituita la larghezza, l'altezza e la profondità in *dest.xyz*.</span><span class="sxs-lookup"><span data-stu-id="15035-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="15035-132">Se *srcResource* è un TextureCube, la larghezza e l'altezza delle dimensioni del singolo cubo vengono restituite in *dest. XY* e *dest. z* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="15035-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="15035-133">Se *srcResource* è un TextureCubeArray, la larghezza e l'altezza delle singole dimensioni del cubo vengono restituite in *dest. XY*.</span><span class="sxs-lookup"><span data-stu-id="15035-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="15035-134">*dest. z* è impostato su un valore non definito.</span><span class="sxs-lookup"><span data-stu-id="15035-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="15035-135">Se il morsetto MIP per risorsa è stato specificato in *srcResource*, ResInfo restituisce sempre il numero totale di mipmap nella visualizzazione per il conteggio MIP, indipendentemente dal morsetto.</span><span class="sxs-lookup"><span data-stu-id="15035-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="15035-136">Tuttavia, se le dimensioni di un determinato miplevel sono richieste da ResInfo e miplevel è stato bloccato, ad esempio un morsetto di 2,2 significa che MIPS 0 e 1 sono stati bloccati, le dimensioni restituite non sono definite.</span><span class="sxs-lookup"><span data-stu-id="15035-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="15035-137">Alcune implementazioni restituiranno il comportamento fuori limite specificato per ResInfo quando miplevel non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="15035-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="15035-138">Altre implementazioni restituiranno le dimensioni del MIP come se non fosse stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="15035-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="15035-139">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="15035-139">Restrictions</span></span>

-   <span data-ttu-id="15035-140">*srcResource* deve essere un \# Registro t o u \# che non sia un buffer, ma è una trama \* .</span><span class="sxs-lookup"><span data-stu-id="15035-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="15035-141">L'indirizzamento relativo di *srcResource* non è consentito.</span><span class="sxs-lookup"><span data-stu-id="15035-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="15035-142">*srcMipLevel* deve usare un selettore di componente singolo se non è un controllo immediato scalare.</span><span class="sxs-lookup"><span data-stu-id="15035-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="15035-143">Il recupero da t \# o u \# a cui non è associato alcun elemento restituisce 0 per Width, Height, depth o arraySize e Total-MIP-Count.</span><span class="sxs-lookup"><span data-stu-id="15035-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="15035-144">Il \_ modificatore rcpFloat viene comunque rispettato in questo caso, restituendo quindi inf per i valori restituiti applicabili.</span><span class="sxs-lookup"><span data-stu-id="15035-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="15035-145">Se *srcMipLevel* non è compreso nell'intervallo del numero disponibile di mipLevels nella risorsa, il comportamento per la dimensione restituita (*dest.xyz*) è identico a quello di una \# risorsa t o u non associata \# .</span><span class="sxs-lookup"><span data-stu-id="15035-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="15035-146">Il numero totale di MIP viene comunque restituito in *dest. w* in questo caso.</span><span class="sxs-lookup"><span data-stu-id="15035-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="15035-147">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="15035-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="15035-148">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="15035-148">Vertex Shader</span></span> | <span data-ttu-id="15035-149">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="15035-149">Geometry Shader</span></span> | <span data-ttu-id="15035-150">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="15035-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="15035-151">x</span><span class="sxs-lookup"><span data-stu-id="15035-151">x</span></span>             | <span data-ttu-id="15035-152">x</span><span class="sxs-lookup"><span data-stu-id="15035-152">x</span></span>               | <span data-ttu-id="15035-153">x</span><span class="sxs-lookup"><span data-stu-id="15035-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15035-154">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="15035-154">Minimum Shader Model</span></span>

<span data-ttu-id="15035-155">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="15035-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15035-156">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="15035-156">Shader Model</span></span>                                              | <span data-ttu-id="15035-157">Supportato</span><span class="sxs-lookup"><span data-stu-id="15035-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="15035-158">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="15035-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="15035-159">sì</span><span class="sxs-lookup"><span data-stu-id="15035-159">yes</span></span>       |
| [<span data-ttu-id="15035-160">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="15035-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="15035-161">sì</span><span class="sxs-lookup"><span data-stu-id="15035-161">yes</span></span>       |
| [<span data-ttu-id="15035-162">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="15035-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="15035-163">sì</span><span class="sxs-lookup"><span data-stu-id="15035-163">yes</span></span>       |
| [<span data-ttu-id="15035-164">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15035-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="15035-165">no</span><span class="sxs-lookup"><span data-stu-id="15035-165">no</span></span>        |
| [<span data-ttu-id="15035-166">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15035-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="15035-167">no</span><span class="sxs-lookup"><span data-stu-id="15035-167">no</span></span>        |
| [<span data-ttu-id="15035-168">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15035-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="15035-169">no</span><span class="sxs-lookup"><span data-stu-id="15035-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="15035-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15035-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15035-171">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15035-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





