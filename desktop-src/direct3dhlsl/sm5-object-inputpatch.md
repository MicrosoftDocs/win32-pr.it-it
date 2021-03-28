---
title: InputPatch
description: Rappresenta una matrice di punti di controllo disponibili per lo scafo dello shader come input.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- HLSL InputPatch
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992888"
---
# <a name="inputpatch"></a><span data-ttu-id="4aa6d-104">InputPatch</span><span class="sxs-lookup"><span data-stu-id="4aa6d-104">InputPatch</span></span>

<span data-ttu-id="4aa6d-105">Rappresenta una matrice di punti di controllo disponibili per lo scafo dello shader come input.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="4aa6d-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-106">Method</span></span>                                                      | <span data-ttu-id="4aa6d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aa6d-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="4aa6d-108">[**Operatore\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4aa6d-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="4aa6d-109">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="4aa6d-110">La classe InputPatch supporta inoltre le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="4aa6d-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="4aa6d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4aa6d-111">Properties</span></span> | <span data-ttu-id="4aa6d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-112">Type</span></span> | <span data-ttu-id="4aa6d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aa6d-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="4aa6d-114">Length</span><span class="sxs-lookup"><span data-stu-id="4aa6d-114">Length</span></span>     | <span data-ttu-id="4aa6d-115">uint</span><span class="sxs-lookup"><span data-stu-id="4aa6d-115">uint</span></span> | <span data-ttu-id="4aa6d-116">Numero di punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4aa6d-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-117">Minimum Shader Model</span></span>

<span data-ttu-id="4aa6d-118">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4aa6d-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4aa6d-119">Shader Model</span></span>                                                                | <span data-ttu-id="4aa6d-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="4aa6d-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4aa6d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="4aa6d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4aa6d-122">sì</span><span class="sxs-lookup"><span data-stu-id="4aa6d-122">yes</span></span>       |



 

<span data-ttu-id="4aa6d-123">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4aa6d-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4aa6d-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="4aa6d-124">Vertex</span></span> | <span data-ttu-id="4aa6d-125">Hull</span><span class="sxs-lookup"><span data-stu-id="4aa6d-125">Hull</span></span> | <span data-ttu-id="4aa6d-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="4aa6d-126">Domain</span></span> | <span data-ttu-id="4aa6d-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="4aa6d-127">Geometry</span></span> | <span data-ttu-id="4aa6d-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4aa6d-128">Pixel</span></span> | <span data-ttu-id="4aa6d-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4aa6d-130">x</span><span class="sxs-lookup"><span data-stu-id="4aa6d-130">x</span></span>    |        | <span data-ttu-id="4aa6d-131">x</span><span class="sxs-lookup"><span data-stu-id="4aa6d-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4aa6d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aa6d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa6d-133">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="4aa6d-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




