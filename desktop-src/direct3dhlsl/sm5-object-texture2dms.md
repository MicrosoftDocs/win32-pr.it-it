---
title: Texture2DMS
description: Il tipo Texture2DMS (esistente nel modello Shader 4) più le variabili di risorsa.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- HLSL Texture2DMS
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045624"
---
# <a name="texture2dms"></a><span data-ttu-id="868b0-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="868b0-104">Texture2DMS</span></span>

<span data-ttu-id="868b0-105">Il tipo Texture2DMS (esistente nel modello Shader 4) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="868b0-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="868b0-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="868b0-106">In this section</span></span>



| <span data-ttu-id="868b0-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="868b0-107">Topic</span></span>                                                                                    | <span data-ttu-id="868b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="868b0-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="868b0-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="868b0-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="868b0-110">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="868b0-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="868b0-111">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="868b0-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="868b0-112">Restituisce la posizione di esempio per l'indice di esempio fornito.</span><span class="sxs-lookup"><span data-stu-id="868b0-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="868b0-113">**Metodi Load**</span><span class="sxs-lookup"><span data-stu-id="868b0-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="868b0-114">Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti.</span><span class="sxs-lookup"><span data-stu-id="868b0-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="868b0-115">[**esempio. Operatore\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="868b0-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="868b0-116">Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti.</span><span class="sxs-lookup"><span data-stu-id="868b0-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="868b0-117">[**Operatore\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="868b0-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="868b0-118">Recupera un valore dalla risorsa nel percorso specificato nell'indice di esempio 0.</span><span class="sxs-lookup"><span data-stu-id="868b0-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="868b0-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="868b0-119">Minimum Shader Model</span></span>

<span data-ttu-id="868b0-120">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="868b0-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="868b0-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="868b0-121">Shader Model</span></span>              | <span data-ttu-id="868b0-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="868b0-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="868b0-123">Shader Model 4 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="868b0-123">Shader model 4 and higher</span></span> | <span data-ttu-id="868b0-124">sì</span><span class="sxs-lookup"><span data-stu-id="868b0-124">yes</span></span>       |



 

<span data-ttu-id="868b0-125">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="868b0-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="868b0-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="868b0-126">Vertex</span></span> | <span data-ttu-id="868b0-127">Hull</span><span class="sxs-lookup"><span data-stu-id="868b0-127">Hull</span></span> | <span data-ttu-id="868b0-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="868b0-128">Domain</span></span> | <span data-ttu-id="868b0-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="868b0-129">Geometry</span></span> | <span data-ttu-id="868b0-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="868b0-130">Pixel</span></span> | <span data-ttu-id="868b0-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="868b0-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="868b0-132">x</span><span class="sxs-lookup"><span data-stu-id="868b0-132">x</span></span>      | <span data-ttu-id="868b0-133">x</span><span class="sxs-lookup"><span data-stu-id="868b0-133">x</span></span>    | <span data-ttu-id="868b0-134">x</span><span class="sxs-lookup"><span data-stu-id="868b0-134">x</span></span>      | <span data-ttu-id="868b0-135">x</span><span class="sxs-lookup"><span data-stu-id="868b0-135">x</span></span>        | <span data-ttu-id="868b0-136">x</span><span class="sxs-lookup"><span data-stu-id="868b0-136">x</span></span>     | <span data-ttu-id="868b0-137">x</span><span class="sxs-lookup"><span data-stu-id="868b0-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="868b0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="868b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868b0-139">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="868b0-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





