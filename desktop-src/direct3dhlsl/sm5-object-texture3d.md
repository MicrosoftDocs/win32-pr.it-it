---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045622"
---
# <a name="texture3d"></a><span data-ttu-id="182a9-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="182a9-104">Texture3D</span></span>

<span data-ttu-id="182a9-105">Il tipo Texture3D ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="182a9-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="182a9-106">Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="182a9-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="182a9-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="182a9-107">Method</span></span>                                                                  | <span data-ttu-id="182a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="182a9-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="182a9-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="182a9-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="182a9-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="182a9-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="182a9-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="182a9-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="182a9-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="182a9-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="182a9-113">[**MIPS. Operatore\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="182a9-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="182a9-114">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="182a9-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="182a9-115">[**Operatore\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="182a9-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="182a9-116">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="182a9-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="182a9-117">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="182a9-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="182a9-118">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="182a9-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="182a9-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="182a9-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="182a9-120">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="182a9-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="182a9-121">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="182a9-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="182a9-122">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="182a9-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="182a9-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="182a9-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="182a9-124">Esegue il campionamento di una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="182a9-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="182a9-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="182a9-125">Minimum Shader Model</span></span>

<span data-ttu-id="182a9-126">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="182a9-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="182a9-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="182a9-127">Shader Model</span></span>                                                                | <span data-ttu-id="182a9-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="182a9-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="182a9-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="182a9-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="182a9-130">sì</span><span class="sxs-lookup"><span data-stu-id="182a9-130">yes</span></span>       |



 

<span data-ttu-id="182a9-131">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="182a9-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="182a9-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="182a9-132">Vertex</span></span> | <span data-ttu-id="182a9-133">Hull</span><span class="sxs-lookup"><span data-stu-id="182a9-133">Hull</span></span> | <span data-ttu-id="182a9-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="182a9-134">Domain</span></span> | <span data-ttu-id="182a9-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="182a9-135">Geometry</span></span> | <span data-ttu-id="182a9-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="182a9-136">Pixel</span></span> | <span data-ttu-id="182a9-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="182a9-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="182a9-138">x</span><span class="sxs-lookup"><span data-stu-id="182a9-138">x</span></span>      | <span data-ttu-id="182a9-139">x</span><span class="sxs-lookup"><span data-stu-id="182a9-139">x</span></span>    | <span data-ttu-id="182a9-140">x</span><span class="sxs-lookup"><span data-stu-id="182a9-140">x</span></span>      | <span data-ttu-id="182a9-141">x</span><span class="sxs-lookup"><span data-stu-id="182a9-141">x</span></span>        | <span data-ttu-id="182a9-142">x</span><span class="sxs-lookup"><span data-stu-id="182a9-142">x</span></span>     | <span data-ttu-id="182a9-143">x</span><span class="sxs-lookup"><span data-stu-id="182a9-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="182a9-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="182a9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182a9-145">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="182a9-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




