---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- HLSL Texture2DArray
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104980999"
---
# <a name="texture2darray"></a><span data-ttu-id="0ea96-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0ea96-104">Texture2DArray</span></span>

<span data-ttu-id="0ea96-105">Il tipo Texture2DArray ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ea96-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="0ea96-106">Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="0ea96-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="0ea96-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="0ea96-107">Method</span></span>                                                                      | <span data-ttu-id="0ea96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ea96-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ea96-109">**Raccogliere**</span><span class="sxs-lookup"><span data-stu-id="0ea96-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="0ea96-110">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="0ea96-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="0ea96-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="0ea96-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="0ea96-112">Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="0ea96-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="0ea96-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="0ea96-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="0ea96-114">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="0ea96-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="0ea96-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="0ea96-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="0ea96-116">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="0ea96-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="0ea96-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="0ea96-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="0ea96-118">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="0ea96-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="0ea96-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="0ea96-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="0ea96-120">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ea96-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="0ea96-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="0ea96-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="0ea96-122">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ea96-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="0ea96-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="0ea96-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="0ea96-124">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ea96-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="0ea96-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="0ea96-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="0ea96-126">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ea96-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="0ea96-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="0ea96-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="0ea96-128">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ea96-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="0ea96-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="0ea96-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="0ea96-130">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ea96-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="0ea96-131">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="0ea96-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="0ea96-132">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="0ea96-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="0ea96-133">[**MIPS. Operatore\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0ea96-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="0ea96-134">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0ea96-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="0ea96-135">[**Operatore\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0ea96-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="0ea96-136">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0ea96-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="0ea96-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0ea96-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="0ea96-138">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="0ea96-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="0ea96-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="0ea96-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="0ea96-140">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="0ea96-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="0ea96-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="0ea96-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="0ea96-142">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="0ea96-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="0ea96-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="0ea96-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="0ea96-144">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="0ea96-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="0ea96-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="0ea96-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="0ea96-146">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="0ea96-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="0ea96-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="0ea96-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="0ea96-148">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="0ea96-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0ea96-149">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0ea96-149">Minimum Shader Model</span></span>

<span data-ttu-id="0ea96-150">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ea96-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0ea96-151">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0ea96-151">Shader Model</span></span>                                                                | <span data-ttu-id="0ea96-152">Supportato</span><span class="sxs-lookup"><span data-stu-id="0ea96-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0ea96-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="0ea96-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0ea96-154">sì</span><span class="sxs-lookup"><span data-stu-id="0ea96-154">yes</span></span>       |



 

<span data-ttu-id="0ea96-155">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ea96-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0ea96-156">Vertice</span><span class="sxs-lookup"><span data-stu-id="0ea96-156">Vertex</span></span> | <span data-ttu-id="0ea96-157">Hull</span><span class="sxs-lookup"><span data-stu-id="0ea96-157">Hull</span></span> | <span data-ttu-id="0ea96-158">Dominio</span><span class="sxs-lookup"><span data-stu-id="0ea96-158">Domain</span></span> | <span data-ttu-id="0ea96-159">Geometria</span><span class="sxs-lookup"><span data-stu-id="0ea96-159">Geometry</span></span> | <span data-ttu-id="0ea96-160">Pixel</span><span class="sxs-lookup"><span data-stu-id="0ea96-160">Pixel</span></span> | <span data-ttu-id="0ea96-161">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0ea96-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0ea96-162">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-162">x</span></span>      | <span data-ttu-id="0ea96-163">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-163">x</span></span>    | <span data-ttu-id="0ea96-164">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-164">x</span></span>      | <span data-ttu-id="0ea96-165">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-165">x</span></span>        | <span data-ttu-id="0ea96-166">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-166">x</span></span>     | <span data-ttu-id="0ea96-167">x</span><span class="sxs-lookup"><span data-stu-id="0ea96-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ea96-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ea96-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea96-169">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="0ea96-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




