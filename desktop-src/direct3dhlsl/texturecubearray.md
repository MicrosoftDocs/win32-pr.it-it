---
title: Oggetto TextureCubeArray
description: Il tipo TextureCubeArray (esistente nel modello Shader 4) più le variabili di risorsa. Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Oggetto TextureCubeArray HLSL
- Oggetto TextureCubeArray HLSL, descritto
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104995245"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="81bce-106">Oggetto TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="81bce-106">TextureCubeArray object</span></span>

<span data-ttu-id="81bce-107">Il tipo **TextureCubeArray** ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="81bce-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="81bce-108">Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="81bce-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="81bce-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="81bce-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81bce-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="81bce-110">Methods</span></span>

<span data-ttu-id="81bce-111">L'oggetto **TextureCubeArray** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="81bce-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="81bce-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="81bce-112">Method</span></span>                                                           | <span data-ttu-id="81bce-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81bce-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81bce-114">**Raccogliere**</span><span class="sxs-lookup"><span data-stu-id="81bce-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="81bce-115">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="81bce-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="81bce-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="81bce-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="81bce-117">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="81bce-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="81bce-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="81bce-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="81bce-119">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="81bce-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="81bce-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="81bce-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="81bce-121">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="81bce-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="81bce-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="81bce-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="81bce-123">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="81bce-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="81bce-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="81bce-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="81bce-125">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="81bce-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="81bce-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="81bce-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="81bce-127">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="81bce-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="81bce-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="81bce-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="81bce-129">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="81bce-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="81bce-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="81bce-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="81bce-131">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="81bce-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="81bce-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="81bce-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="81bce-133">Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="81bce-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="81bce-134">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="81bce-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="81bce-135">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="81bce-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="81bce-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="81bce-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="81bce-137">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="81bce-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="81bce-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="81bce-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="81bce-139">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="81bce-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="81bce-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="81bce-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="81bce-141">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="81bce-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="81bce-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="81bce-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="81bce-143">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="81bce-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="81bce-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="81bce-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="81bce-145">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="81bce-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="81bce-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="81bce-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="81bce-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="81bce-147">Minimum Shader Model</span></span>

<span data-ttu-id="81bce-148">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="81bce-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="81bce-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="81bce-149">Shader Model</span></span>                                                                | <span data-ttu-id="81bce-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="81bce-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="81bce-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="81bce-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="81bce-152">sì</span><span class="sxs-lookup"><span data-stu-id="81bce-152">yes</span></span>       |



 

<span data-ttu-id="81bce-153">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="81bce-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="81bce-154">Vertice</span><span class="sxs-lookup"><span data-stu-id="81bce-154">Vertex</span></span> | <span data-ttu-id="81bce-155">Hull</span><span class="sxs-lookup"><span data-stu-id="81bce-155">Hull</span></span> | <span data-ttu-id="81bce-156">Dominio</span><span class="sxs-lookup"><span data-stu-id="81bce-156">Domain</span></span> | <span data-ttu-id="81bce-157">Geometria</span><span class="sxs-lookup"><span data-stu-id="81bce-157">Geometry</span></span> | <span data-ttu-id="81bce-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="81bce-158">Pixel</span></span> | <span data-ttu-id="81bce-159">Calcolo</span><span class="sxs-lookup"><span data-stu-id="81bce-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="81bce-160">x</span><span class="sxs-lookup"><span data-stu-id="81bce-160">x</span></span>      | <span data-ttu-id="81bce-161">x</span><span class="sxs-lookup"><span data-stu-id="81bce-161">x</span></span>    | <span data-ttu-id="81bce-162">x</span><span class="sxs-lookup"><span data-stu-id="81bce-162">x</span></span>      | <span data-ttu-id="81bce-163">x</span><span class="sxs-lookup"><span data-stu-id="81bce-163">x</span></span>        | <span data-ttu-id="81bce-164">x</span><span class="sxs-lookup"><span data-stu-id="81bce-164">x</span></span>     | <span data-ttu-id="81bce-165">x</span><span class="sxs-lookup"><span data-stu-id="81bce-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="81bce-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81bce-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bce-167">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="81bce-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





