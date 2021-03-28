---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- HLSL OutputPatch
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045584"
---
# <a name="outputpatch"></a><span data-ttu-id="6e53a-104">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="6e53a-104">OutputPatch</span></span>

<span data-ttu-id="6e53a-105">Rappresenta una matrice di punti di controllo di output disponibili per la funzione patch-Constant di Hull shader e per lo shader del dominio.</span><span class="sxs-lookup"><span data-stu-id="6e53a-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="6e53a-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="6e53a-106">Method</span></span>                                                       | <span data-ttu-id="6e53a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e53a-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="6e53a-108">[**Operatore\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="6e53a-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="6e53a-109">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6e53a-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="6e53a-110">Inoltre, la classe InputPatch supporta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e53a-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="6e53a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6e53a-111">Properties</span></span> | <span data-ttu-id="6e53a-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e53a-112">Type</span></span> | <span data-ttu-id="6e53a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e53a-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="6e53a-114">Length</span><span class="sxs-lookup"><span data-stu-id="6e53a-114">Length</span></span>     | <span data-ttu-id="6e53a-115">uint</span><span class="sxs-lookup"><span data-stu-id="6e53a-115">uint</span></span> | <span data-ttu-id="6e53a-116">Numero di punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="6e53a-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6e53a-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6e53a-117">Minimum Shader Model</span></span>

<span data-ttu-id="6e53a-118">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e53a-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6e53a-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6e53a-119">Shader Model</span></span>                                                                | <span data-ttu-id="6e53a-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="6e53a-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6e53a-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="6e53a-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6e53a-122">sì</span><span class="sxs-lookup"><span data-stu-id="6e53a-122">yes</span></span>       |



 

<span data-ttu-id="6e53a-123">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e53a-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6e53a-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="6e53a-124">Vertex</span></span> | <span data-ttu-id="6e53a-125">Hull</span><span class="sxs-lookup"><span data-stu-id="6e53a-125">Hull</span></span> | <span data-ttu-id="6e53a-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="6e53a-126">Domain</span></span> | <span data-ttu-id="6e53a-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="6e53a-127">Geometry</span></span> | <span data-ttu-id="6e53a-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="6e53a-128">Pixel</span></span> | <span data-ttu-id="6e53a-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6e53a-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="6e53a-130">x</span><span class="sxs-lookup"><span data-stu-id="6e53a-130">x</span></span>    | <span data-ttu-id="6e53a-131">x</span><span class="sxs-lookup"><span data-stu-id="6e53a-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="6e53a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e53a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e53a-133">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="6e53a-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




