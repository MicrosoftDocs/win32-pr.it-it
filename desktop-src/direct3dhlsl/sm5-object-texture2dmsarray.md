---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- HLSL Texture2DMSArray
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104234462"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="096d6-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="096d6-104">Texture2DMSArray</span></span>

<span data-ttu-id="096d6-105">Il tipo Texture2DMSArray (esistente nel modello Shader 4) più le variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="096d6-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="096d6-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="096d6-106">Method</span></span>                                                                             | <span data-ttu-id="096d6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="096d6-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="096d6-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="096d6-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="096d6-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="096d6-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="096d6-110">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="096d6-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="096d6-111">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="096d6-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="096d6-112">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="096d6-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="096d6-113">Ottiene un valore.</span><span class="sxs-lookup"><span data-stu-id="096d6-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="096d6-114">[**esempio. Operatore\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="096d6-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="096d6-115">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="096d6-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="096d6-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="096d6-116">Minimum Shader Model</span></span>

<span data-ttu-id="096d6-117">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="096d6-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="096d6-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="096d6-118">Shader Model</span></span>                                                                | <span data-ttu-id="096d6-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="096d6-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="096d6-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="096d6-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="096d6-121">sì</span><span class="sxs-lookup"><span data-stu-id="096d6-121">yes</span></span>       |



 

<span data-ttu-id="096d6-122">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="096d6-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="096d6-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="096d6-123">Vertex</span></span> | <span data-ttu-id="096d6-124">Hull</span><span class="sxs-lookup"><span data-stu-id="096d6-124">Hull</span></span> | <span data-ttu-id="096d6-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="096d6-125">Domain</span></span> | <span data-ttu-id="096d6-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="096d6-126">Geometry</span></span> | <span data-ttu-id="096d6-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="096d6-127">Pixel</span></span> | <span data-ttu-id="096d6-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="096d6-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="096d6-129">x</span><span class="sxs-lookup"><span data-stu-id="096d6-129">x</span></span>      | <span data-ttu-id="096d6-130">x</span><span class="sxs-lookup"><span data-stu-id="096d6-130">x</span></span>    | <span data-ttu-id="096d6-131">x</span><span class="sxs-lookup"><span data-stu-id="096d6-131">x</span></span>      | <span data-ttu-id="096d6-132">x</span><span class="sxs-lookup"><span data-stu-id="096d6-132">x</span></span>        | <span data-ttu-id="096d6-133">x</span><span class="sxs-lookup"><span data-stu-id="096d6-133">x</span></span>     | <span data-ttu-id="096d6-134">x</span><span class="sxs-lookup"><span data-stu-id="096d6-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="096d6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="096d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096d6-136">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="096d6-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




