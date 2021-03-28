---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- HLSL Texture1DArray
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045852"
---
# <a name="texture1darray"></a><span data-ttu-id="07c97-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="07c97-104">Texture1DArray</span></span>

<span data-ttu-id="07c97-105">Il tipo Texture1DArray ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="07c97-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="07c97-106">Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="07c97-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="07c97-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="07c97-107">Method</span></span>                                                                       | <span data-ttu-id="07c97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07c97-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07c97-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="07c97-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="07c97-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="07c97-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="07c97-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="07c97-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="07c97-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="07c97-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="07c97-113">[**MIPS. Operatore\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="07c97-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="07c97-114">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07c97-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="07c97-115">[**Operatore\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="07c97-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="07c97-116">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07c97-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="07c97-117">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="07c97-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="07c97-118">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="07c97-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="07c97-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="07c97-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="07c97-120">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="07c97-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="07c97-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="07c97-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="07c97-122">Campiona una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="07c97-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="07c97-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="07c97-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="07c97-124">Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="07c97-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="07c97-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="07c97-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="07c97-126">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="07c97-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="07c97-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="07c97-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="07c97-128">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="07c97-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="07c97-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="07c97-129">Minimum Shader Model</span></span>

<span data-ttu-id="07c97-130">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="07c97-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="07c97-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="07c97-131">Shader Model</span></span>                                                                | <span data-ttu-id="07c97-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="07c97-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="07c97-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="07c97-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="07c97-134">sì</span><span class="sxs-lookup"><span data-stu-id="07c97-134">yes</span></span>       |



 

<span data-ttu-id="07c97-135">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="07c97-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="07c97-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="07c97-136">Vertex</span></span> | <span data-ttu-id="07c97-137">Hull</span><span class="sxs-lookup"><span data-stu-id="07c97-137">Hull</span></span> | <span data-ttu-id="07c97-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="07c97-138">Domain</span></span> | <span data-ttu-id="07c97-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="07c97-139">Geometry</span></span> | <span data-ttu-id="07c97-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="07c97-140">Pixel</span></span> | <span data-ttu-id="07c97-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="07c97-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="07c97-142">x</span><span class="sxs-lookup"><span data-stu-id="07c97-142">x</span></span>      | <span data-ttu-id="07c97-143">x</span><span class="sxs-lookup"><span data-stu-id="07c97-143">x</span></span>    | <span data-ttu-id="07c97-144">x</span><span class="sxs-lookup"><span data-stu-id="07c97-144">x</span></span>      | <span data-ttu-id="07c97-145">x</span><span class="sxs-lookup"><span data-stu-id="07c97-145">x</span></span>        | <span data-ttu-id="07c97-146">x</span><span class="sxs-lookup"><span data-stu-id="07c97-146">x</span></span>     | <span data-ttu-id="07c97-147">x</span><span class="sxs-lookup"><span data-stu-id="07c97-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="07c97-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07c97-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c97-149">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="07c97-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




