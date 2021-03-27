---
title: Oggetto TextureCube
description: Il tipo TextureCube (esistente nel modello Shader 4) più le variabili di risorsa. Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Oggetto TextureCube HLSL
- Oggetto TextureCube HLSL, descritto
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104132138"
---
# <a name="texturecube-object"></a><span data-ttu-id="b72ca-106">Oggetto TextureCube</span><span class="sxs-lookup"><span data-stu-id="b72ca-106">TextureCube object</span></span>

<span data-ttu-id="b72ca-107">Il tipo **TextureCube** ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b72ca-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="b72ca-108">Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="b72ca-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="b72ca-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="b72ca-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b72ca-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b72ca-110">Methods</span></span>

<span data-ttu-id="b72ca-111">L'oggetto **TextureCube** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b72ca-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="b72ca-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="b72ca-112">Method</span></span>                                                      | <span data-ttu-id="b72ca-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b72ca-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b72ca-114">**Raccogliere**</span><span class="sxs-lookup"><span data-stu-id="b72ca-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="b72ca-115">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="b72ca-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="b72ca-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="b72ca-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="b72ca-117">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="b72ca-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="b72ca-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="b72ca-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="b72ca-119">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="b72ca-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="b72ca-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="b72ca-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="b72ca-121">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b72ca-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="b72ca-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="b72ca-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="b72ca-123">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b72ca-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="b72ca-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="b72ca-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="b72ca-125">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b72ca-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="b72ca-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="b72ca-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="b72ca-127">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b72ca-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="b72ca-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="b72ca-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="b72ca-129">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b72ca-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="b72ca-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="b72ca-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="b72ca-131">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="b72ca-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="b72ca-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="b72ca-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="b72ca-133">Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="b72ca-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="b72ca-134">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b72ca-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="b72ca-135">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="b72ca-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="b72ca-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="b72ca-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="b72ca-137">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="b72ca-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="b72ca-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="b72ca-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="b72ca-139">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="b72ca-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="b72ca-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="b72ca-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="b72ca-141">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="b72ca-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="b72ca-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="b72ca-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="b72ca-143">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="b72ca-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="b72ca-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="b72ca-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="b72ca-145">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="b72ca-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b72ca-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="b72ca-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b72ca-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b72ca-147">Minimum Shader Model</span></span>

<span data-ttu-id="b72ca-148">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b72ca-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b72ca-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b72ca-149">Shader Model</span></span>                                                                | <span data-ttu-id="b72ca-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="b72ca-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b72ca-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="b72ca-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b72ca-152">sì</span><span class="sxs-lookup"><span data-stu-id="b72ca-152">yes</span></span>       |



 

<span data-ttu-id="b72ca-153">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b72ca-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b72ca-154">Vertice</span><span class="sxs-lookup"><span data-stu-id="b72ca-154">Vertex</span></span> | <span data-ttu-id="b72ca-155">Hull</span><span class="sxs-lookup"><span data-stu-id="b72ca-155">Hull</span></span> | <span data-ttu-id="b72ca-156">Dominio</span><span class="sxs-lookup"><span data-stu-id="b72ca-156">Domain</span></span> | <span data-ttu-id="b72ca-157">Geometria</span><span class="sxs-lookup"><span data-stu-id="b72ca-157">Geometry</span></span> | <span data-ttu-id="b72ca-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="b72ca-158">Pixel</span></span> | <span data-ttu-id="b72ca-159">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b72ca-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b72ca-160">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-160">x</span></span>      | <span data-ttu-id="b72ca-161">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-161">x</span></span>    | <span data-ttu-id="b72ca-162">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-162">x</span></span>      | <span data-ttu-id="b72ca-163">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-163">x</span></span>        | <span data-ttu-id="b72ca-164">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-164">x</span></span>     | <span data-ttu-id="b72ca-165">x</span><span class="sxs-lookup"><span data-stu-id="b72ca-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b72ca-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b72ca-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72ca-167">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="b72ca-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





