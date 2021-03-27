---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- HLSL Texture2D
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104981015"
---
# <a name="texture2d"></a><span data-ttu-id="957d1-104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="957d1-104">Texture2D</span></span>

<span data-ttu-id="957d1-105">Il tipo Texture2D ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="957d1-105">Texture2D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="957d1-106">Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="957d1-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="957d1-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="957d1-107">Method</span></span>                                                                 | <span data-ttu-id="957d1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="957d1-108">Description</span></span>                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="957d1-109">**Raccogliere**</span><span class="sxs-lookup"><span data-stu-id="957d1-109">**Gather**</span></span>](texture2d-gather.md)                                      | <span data-ttu-id="957d1-110">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="957d1-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="957d1-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="957d1-111">**GatherRed**</span></span>](texture2d-gatherred.md)                                | <span data-ttu-id="957d1-112">Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="957d1-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="957d1-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="957d1-113">**GatherGreen**</span></span>](texture2d-gathergreen.md)                            | <span data-ttu-id="957d1-114">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="957d1-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="957d1-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="957d1-115">**GatherBlue**</span></span>](texture2d-gatherblue.md)                              | <span data-ttu-id="957d1-116">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="957d1-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="957d1-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="957d1-117">**GatherAlpha**</span></span>](texture2d-gatheralpha.md)                            | <span data-ttu-id="957d1-118">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="957d1-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="957d1-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="957d1-119">**GatherCmp**</span></span>](texture2d-gathercmp.md)                                | <span data-ttu-id="957d1-120">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="957d1-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="957d1-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="957d1-121">**GatherCmpRed**</span></span>](texture2d-gathercmpred.md)                          | <span data-ttu-id="957d1-122">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="957d1-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="957d1-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="957d1-123">**GatherCmpGreen**</span></span>](texture2d-gathercmpgreen.md)                      | <span data-ttu-id="957d1-124">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="957d1-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="957d1-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="957d1-125">**GatherCmpBlue**</span></span>](texture2d-gathercmpblue.md)                        | <span data-ttu-id="957d1-126">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="957d1-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="957d1-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="957d1-127">**GatherCmpAlpha**</span></span>](texture2d-gathercmpalpha.md)                      | <span data-ttu-id="957d1-128">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="957d1-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="957d1-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="957d1-129">**GetDimensions**</span></span>](sm5-object-texture2d-getdimensions.md)             | <span data-ttu-id="957d1-130">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="957d1-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="957d1-131">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="957d1-131">**Load**</span></span>](texture2d-load.md)                                          | <span data-ttu-id="957d1-132">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="957d1-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="957d1-133">[**MIPS. Operatore\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="957d1-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="957d1-134">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="957d1-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="957d1-135">[**Operatore\[\]**](sm5-object-texture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="957d1-135">[**Operator\[\]**](sm5-object-texture2d-operatorindex.md)</span></span>              | <span data-ttu-id="957d1-136">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="957d1-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="957d1-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="957d1-137">**Sample**</span></span>](texture-sample-overload.md)                               | <span data-ttu-id="957d1-138">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="957d1-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="957d1-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="957d1-139">**SampleBias**</span></span>](texture2d-samplebias.md)                              | <span data-ttu-id="957d1-140">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="957d1-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="957d1-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="957d1-141">**SampleCmp**</span></span>](texture2d-samplecmp.md)                                | <span data-ttu-id="957d1-142">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="957d1-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="957d1-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="957d1-143">**SampleCmpLevelZero**</span></span>](texture2d-samplecmplevelzero.md)              | <span data-ttu-id="957d1-144">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="957d1-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="957d1-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="957d1-145">**SampleGrad**</span></span>](texture2d-samplegrad.md)                              | <span data-ttu-id="957d1-146">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="957d1-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="957d1-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="957d1-147">**SampleLevel**</span></span>](texture2d-samplelevel.md)                            | <span data-ttu-id="957d1-148">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="957d1-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="957d1-149">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="957d1-149">Minimum Shader Model</span></span>

<span data-ttu-id="957d1-150">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="957d1-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="957d1-151">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="957d1-151">Shader Model</span></span>                                                                | <span data-ttu-id="957d1-152">Supportato</span><span class="sxs-lookup"><span data-stu-id="957d1-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="957d1-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="957d1-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="957d1-154">sì</span><span class="sxs-lookup"><span data-stu-id="957d1-154">yes</span></span>       |



 

<span data-ttu-id="957d1-155">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="957d1-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="957d1-156">Vertice</span><span class="sxs-lookup"><span data-stu-id="957d1-156">Vertex</span></span> | <span data-ttu-id="957d1-157">Hull</span><span class="sxs-lookup"><span data-stu-id="957d1-157">Hull</span></span> | <span data-ttu-id="957d1-158">Dominio</span><span class="sxs-lookup"><span data-stu-id="957d1-158">Domain</span></span> | <span data-ttu-id="957d1-159">Geometria</span><span class="sxs-lookup"><span data-stu-id="957d1-159">Geometry</span></span> | <span data-ttu-id="957d1-160">Pixel</span><span class="sxs-lookup"><span data-stu-id="957d1-160">Pixel</span></span> | <span data-ttu-id="957d1-161">Calcolo</span><span class="sxs-lookup"><span data-stu-id="957d1-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="957d1-162">x</span><span class="sxs-lookup"><span data-stu-id="957d1-162">x</span></span>      | <span data-ttu-id="957d1-163">x</span><span class="sxs-lookup"><span data-stu-id="957d1-163">x</span></span>    | <span data-ttu-id="957d1-164">x</span><span class="sxs-lookup"><span data-stu-id="957d1-164">x</span></span>      | <span data-ttu-id="957d1-165">x</span><span class="sxs-lookup"><span data-stu-id="957d1-165">x</span></span>        | <span data-ttu-id="957d1-166">x</span><span class="sxs-lookup"><span data-stu-id="957d1-166">x</span></span>     | <span data-ttu-id="957d1-167">x</span><span class="sxs-lookup"><span data-stu-id="957d1-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="957d1-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="957d1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957d1-169">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="957d1-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




