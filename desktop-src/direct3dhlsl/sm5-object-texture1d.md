---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955999"
---
# <a name="texture1d"></a><span data-ttu-id="eb0ff-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="eb0ff-104">Texture1D</span></span>

<span data-ttu-id="eb0ff-105">Un tipo di trama 1D ([presente in Shader Model 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="eb0ff-106">Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="eb0ff-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="eb0ff-107">Method</span></span>                                                                  | <span data-ttu-id="eb0ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb0ff-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb0ff-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="eb0ff-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="eb0ff-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="eb0ff-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="eb0ff-113">[**Operatore\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="eb0ff-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="eb0ff-114">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="eb0ff-115">[**MIPS. Operatore\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="eb0ff-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="eb0ff-116">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="eb0ff-117">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="eb0ff-118">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="eb0ff-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="eb0ff-120">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="eb0ff-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="eb0ff-122">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="eb0ff-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="eb0ff-124">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="eb0ff-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="eb0ff-126">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="eb0ff-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="eb0ff-128">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb0ff-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="eb0ff-129">Minimum Shader Model</span></span>

<span data-ttu-id="eb0ff-130">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb0ff-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="eb0ff-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="eb0ff-131">Shader Model</span></span>                                                                | <span data-ttu-id="eb0ff-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="eb0ff-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="eb0ff-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="eb0ff-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="eb0ff-134">sì</span><span class="sxs-lookup"><span data-stu-id="eb0ff-134">yes</span></span>       |



 

<span data-ttu-id="eb0ff-135">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb0ff-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eb0ff-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="eb0ff-136">Vertex</span></span> | <span data-ttu-id="eb0ff-137">Hull</span><span class="sxs-lookup"><span data-stu-id="eb0ff-137">Hull</span></span> | <span data-ttu-id="eb0ff-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="eb0ff-138">Domain</span></span> | <span data-ttu-id="eb0ff-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="eb0ff-139">Geometry</span></span> | <span data-ttu-id="eb0ff-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="eb0ff-140">Pixel</span></span> | <span data-ttu-id="eb0ff-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="eb0ff-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eb0ff-142">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-142">x</span></span>      | <span data-ttu-id="eb0ff-143">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-143">x</span></span>    | <span data-ttu-id="eb0ff-144">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-144">x</span></span>      | <span data-ttu-id="eb0ff-145">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-145">x</span></span>        | <span data-ttu-id="eb0ff-146">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-146">x</span></span>     | <span data-ttu-id="eb0ff-147">x</span><span class="sxs-lookup"><span data-stu-id="eb0ff-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eb0ff-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb0ff-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0ff-149">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="eb0ff-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




