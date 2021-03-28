---
title: sample_c (SM4-ASM)
description: Esegue un filtro di confronto.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993024"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="7e863-103">esempio \_ c (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7e863-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="7e863-104">Esegue un filtro di confronto.</span><span class="sxs-lookup"><span data-stu-id="7e863-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="7e863-105">esempio \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//deve essere. r swizzle srcSampler, srcReferenceValue//componente singolo selezionato</span><span class="sxs-lookup"><span data-stu-id="7e863-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7e863-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e863-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="7e863-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e863-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e863-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7e863-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="7e863-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7e863-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="7e863-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="7e863-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="7e863-111">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7e863-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="7e863-112">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7e863-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="7e863-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="7e863-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="7e863-114">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="7e863-114">\[in\] A texture register.</span></span> <span data-ttu-id="7e863-115">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="7e863-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7e863-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="7e863-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="7e863-117">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="7e863-117">\[in\] A sampler register.</span></span> <span data-ttu-id="7e863-118">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="7e863-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7e863-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="7e863-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="7e863-120">\[in \] un registro con un singolo componente selezionato, che viene utilizzato nel confronto.</span><span class="sxs-lookup"><span data-stu-id="7e863-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7e863-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e863-121">Remarks</span></span>

<span data-ttu-id="7e863-122">Lo scopo principale di questa istruzione è fornire un blocco predefinito per Percentage-Closer filtro di profondità.</span><span class="sxs-lookup"><span data-stu-id="7e863-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="7e863-123">"C" nell' **esempio \_ c** sta per essere confrontato.</span><span class="sxs-lookup"><span data-stu-id="7e863-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="7e863-124">Gli operandi dell' **esempio \_ c** sono identici a quelli dell'istruzione di [esempio](sample--sm4---asm-.md) , ad eccezione del fatto che esiste un operando di origine float32 aggiuntivo, *srcReferenceValue*, che deve essere un registro con un solo componente selezionato o un valore letterale scalare.</span><span class="sxs-lookup"><span data-stu-id="7e863-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="7e863-125">Il parametro *srcResource* deve avere un Swizzle. r (rosso).</span><span class="sxs-lookup"><span data-stu-id="7e863-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="7e863-126">l' **esempio \_ c** opera esclusivamente sul componente rosso e restituisce un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="7e863-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="7e863-127">Il. r swizzle su *srcResource* indica che il risultato scalare viene replicato in tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="7e863-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="7e863-128">Quando un buffer di profondità viene impostato come trama di input, il valore di profondità viene visualizzato nel componente rosso.</span><span class="sxs-lookup"><span data-stu-id="7e863-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="7e863-129">Se questa istruzione viene usata con una risorsa che non è Texture1D/2D/2DArray/Cube/CubeArray, genera risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="7e863-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="7e863-130">Quando questa istruzione viene eseguita, l'hardware di campionamento usa il ComparisonFunction del campionatore corrente per confrontare *srcReferenceValue* con il valore del componente rosso per la risorsa di origine in ogni filtro "Tap" location (Texel) che il filtro di trama attualmente configurato copre, in base alle coordinate specificate in *srcAddress*.</span><span class="sxs-lookup"><span data-stu-id="7e863-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="7e863-131">Il confronto si verifica dopo che *srcReferenceValue* è stato quantizzato alla precisione del formato di trama, nello stesso modo in cui z è quantizzato alla precisione del buffer di profondità prima del confronto di profondità nel test di visibilità della fusione di output.</span><span class="sxs-lookup"><span data-stu-id="7e863-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="7e863-132">Questo include un morsetto nell'intervallo di formato (ad esempio, \[ 0.. 1 \] per un formato UNORM).</span><span class="sxs-lookup"><span data-stu-id="7e863-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="7e863-133">Il componente rosso di Texel di origine viene confrontato con il *srcReferenceValue* quantizzato.</span><span class="sxs-lookup"><span data-stu-id="7e863-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="7e863-134">Per i Texel che esulano dalla risorsa, il valore del componente rosso viene determinato applicando le modalità di indirizzo (e BorderColorR se in modalità bordo) dal campionatore.</span><span class="sxs-lookup"><span data-stu-id="7e863-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="7e863-135">Il confronto rispetta tutte le regole di confronto a virgola mobile D3D11, nel caso in cui il formato di trama sia a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7e863-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="7e863-136">Ogni confronto che passa restituisce 1,0 f come valore del componente rosso per il Texel e ogni confronto che ha esito negativo restituisce 0,0 f come valore rosso per la trama.</span><span class="sxs-lookup"><span data-stu-id="7e863-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="7e863-137">Il filtro viene quindi eseguito esattamente come specificato dagli Stati del campionatore, operativo solo nel componente rosso e restituendo un singolo filtro scalare allo shader, replicato in tutti i componenti *dest* mascherati.</span><span class="sxs-lookup"><span data-stu-id="7e863-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="7e863-138">L'uso dell' **esempio \_ c** è ortogonale per tutti gli altri controlli di filtro per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="7e863-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="7e863-139">l' **esempio \_ c** funziona senza interruzioni con le altre modalità di filtro per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="7e863-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="7e863-140">nell' **esempio \_ c** il comportamento dei filtri per utilizzo generico viene modificato in modo che i valori filtrati diventino tutti 1,0 f o 0,0 f a causa di risultati di confronto.</span><span class="sxs-lookup"><span data-stu-id="7e863-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="7e863-141">Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="7e863-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="7e863-142">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7e863-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="7e863-143">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e863-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e863-144">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="7e863-144">Vertex Shader</span></span> | <span data-ttu-id="7e863-145">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="7e863-145">Geometry Shader</span></span> | <span data-ttu-id="7e863-146">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="7e863-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="7e863-147">x</span><span class="sxs-lookup"><span data-stu-id="7e863-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e863-148">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7e863-148">Minimum Shader Model</span></span>

<span data-ttu-id="7e863-149">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7e863-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7e863-150">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7e863-150">Shader Model</span></span>                                              | <span data-ttu-id="7e863-151">Supportato</span><span class="sxs-lookup"><span data-stu-id="7e863-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e863-152">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7e863-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e863-153">sì</span><span class="sxs-lookup"><span data-stu-id="7e863-153">yes</span></span>       |
| [<span data-ttu-id="7e863-154">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7e863-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e863-155">sì</span><span class="sxs-lookup"><span data-stu-id="7e863-155">yes</span></span>       |
| [<span data-ttu-id="7e863-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7e863-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e863-157">sì</span><span class="sxs-lookup"><span data-stu-id="7e863-157">yes</span></span>       |
| [<span data-ttu-id="7e863-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e863-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e863-159">no</span><span class="sxs-lookup"><span data-stu-id="7e863-159">no</span></span>        |
| [<span data-ttu-id="7e863-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e863-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e863-161">no</span><span class="sxs-lookup"><span data-stu-id="7e863-161">no</span></span>        |
| [<span data-ttu-id="7e863-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e863-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e863-163">no</span><span class="sxs-lookup"><span data-stu-id="7e863-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e863-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e863-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e863-165">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e863-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





