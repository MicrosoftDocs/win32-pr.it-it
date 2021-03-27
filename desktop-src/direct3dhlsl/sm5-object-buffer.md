---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- Buffer HLSL
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397863"
---
# <a name="buffer"></a><span data-ttu-id="7223f-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="7223f-104">Buffer</span></span>

<span data-ttu-id="7223f-105">Il tipo di buffer esiste nel modello Shader 4 più le variabili di risorsa e le informazioni sul buffer.</span><span class="sxs-lookup"><span data-stu-id="7223f-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="7223f-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="7223f-106">Method</span></span>                                                   | <span data-ttu-id="7223f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7223f-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="7223f-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="7223f-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="7223f-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7223f-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="7223f-110">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="7223f-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="7223f-111">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="7223f-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="7223f-112">[**Operatore\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="7223f-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="7223f-113">Ottiene una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7223f-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7223f-114">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7223f-114">Minimum Shader Model</span></span>

<span data-ttu-id="7223f-115">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7223f-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="7223f-116">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7223f-116">Shader Model</span></span>                                                                | <span data-ttu-id="7223f-117">Supportato</span><span class="sxs-lookup"><span data-stu-id="7223f-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7223f-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="7223f-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7223f-119">sì</span><span class="sxs-lookup"><span data-stu-id="7223f-119">yes</span></span>       |



 

<span data-ttu-id="7223f-120">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7223f-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7223f-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="7223f-121">Vertex</span></span> | <span data-ttu-id="7223f-122">Hull</span><span class="sxs-lookup"><span data-stu-id="7223f-122">Hull</span></span> | <span data-ttu-id="7223f-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="7223f-123">Domain</span></span> | <span data-ttu-id="7223f-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="7223f-124">Geometry</span></span> | <span data-ttu-id="7223f-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="7223f-125">Pixel</span></span> | <span data-ttu-id="7223f-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7223f-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7223f-127">x</span><span class="sxs-lookup"><span data-stu-id="7223f-127">x</span></span>      | <span data-ttu-id="7223f-128">x</span><span class="sxs-lookup"><span data-stu-id="7223f-128">x</span></span>    | <span data-ttu-id="7223f-129">x</span><span class="sxs-lookup"><span data-stu-id="7223f-129">x</span></span>      | <span data-ttu-id="7223f-130">x</span><span class="sxs-lookup"><span data-stu-id="7223f-130">x</span></span>        | <span data-ttu-id="7223f-131">x</span><span class="sxs-lookup"><span data-stu-id="7223f-131">x</span></span>     | <span data-ttu-id="7223f-132">x</span><span class="sxs-lookup"><span data-stu-id="7223f-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7223f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7223f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7223f-134">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="7223f-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




