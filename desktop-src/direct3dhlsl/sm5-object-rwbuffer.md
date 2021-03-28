---
title: RWBuffer
description: Un buffer di lettura/scrittura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL RWBuffer
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334039"
---
# <a name="rwbuffer"></a><span data-ttu-id="621b0-104">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="621b0-104">RWBuffer</span></span>

<span data-ttu-id="621b0-105">Un buffer di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="621b0-105">A read/write buffer.</span></span>



| <span data-ttu-id="621b0-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="621b0-106">Method</span></span>                                                     | <span data-ttu-id="621b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="621b0-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="621b0-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="621b0-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="621b0-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="621b0-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="621b0-110">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="621b0-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="621b0-111">Ottiene un valore in un buffer di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="621b0-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="621b0-112">[**Operatore\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="621b0-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="621b0-113">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="621b0-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="621b0-114">Una variabile di risorsa può essere passata anche in qualsiasi operazione non ordinata o Interlocked.</span><span class="sxs-lookup"><span data-stu-id="621b0-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="621b0-115">Gli oggetti **RWBuffer** possono essere preceduti dalla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="621b0-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="621b0-116">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="621b0-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="621b0-117">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="621b0-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="621b0-118">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="621b0-118">Minimum Shader Model</span></span>

<span data-ttu-id="621b0-119">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="621b0-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="621b0-120">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="621b0-120">Shader Model</span></span>                                                                | <span data-ttu-id="621b0-121">Supportato</span><span class="sxs-lookup"><span data-stu-id="621b0-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="621b0-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="621b0-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="621b0-123">sì</span><span class="sxs-lookup"><span data-stu-id="621b0-123">yes</span></span>       |



 

<span data-ttu-id="621b0-124">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="621b0-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="621b0-125">Vertice</span><span class="sxs-lookup"><span data-stu-id="621b0-125">Vertex</span></span> | <span data-ttu-id="621b0-126">Hull</span><span class="sxs-lookup"><span data-stu-id="621b0-126">Hull</span></span> | <span data-ttu-id="621b0-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="621b0-127">Domain</span></span> | <span data-ttu-id="621b0-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="621b0-128">Geometry</span></span> | <span data-ttu-id="621b0-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="621b0-129">Pixel</span></span> | <span data-ttu-id="621b0-130">Calcolo</span><span class="sxs-lookup"><span data-stu-id="621b0-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="621b0-131">x</span><span class="sxs-lookup"><span data-stu-id="621b0-131">x</span></span>     | <span data-ttu-id="621b0-132">x</span><span class="sxs-lookup"><span data-stu-id="621b0-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="621b0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="621b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621b0-134">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="621b0-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




