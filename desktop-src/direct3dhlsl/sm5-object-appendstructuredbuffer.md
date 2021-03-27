---
title: AppendStructuredBuffer
description: Buffer di output visualizzato come flusso a cui è possibile aggiungere lo shader. Solo i buffer strutturati possono assumere tipi T che sono strutture.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- HLSL AppendStructuredBuffer
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728186"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="d4ffb-105">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="d4ffb-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="d4ffb-106">Buffer di output visualizzato come flusso a cui è possibile aggiungere lo shader.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="d4ffb-107">Solo i buffer strutturati possono assumere tipi T che sono strutture.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="d4ffb-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="d4ffb-108">Method</span></span>                                                                   | <span data-ttu-id="d4ffb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4ffb-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d4ffb-110">**Accodamento**</span><span class="sxs-lookup"><span data-stu-id="d4ffb-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="d4ffb-111">Aggiunge un valore alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="d4ffb-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="d4ffb-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="d4ffb-113">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="d4ffb-114">Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="d4ffb-115">È necessario che l'UAV associato a questa risorsa sia stato creato con l' [**\_ \_ \_ \_ aggiunta del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="d4ffb-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="d4ffb-116">Per ulteriori informazioni su un buffer strutturato di Accodamento, vedere entrambe le sezioni: [Accodamento e utilizzo del buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e del [buffer strutturato](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="d4ffb-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d4ffb-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d4ffb-117">Minimum Shader Model</span></span>

<span data-ttu-id="d4ffb-118">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4ffb-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d4ffb-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d4ffb-119">Shader Model</span></span>                                                                | <span data-ttu-id="d4ffb-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="d4ffb-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d4ffb-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="d4ffb-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d4ffb-122">sì</span><span class="sxs-lookup"><span data-stu-id="d4ffb-122">yes</span></span>       |



 

<span data-ttu-id="d4ffb-123">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4ffb-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d4ffb-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="d4ffb-124">Vertex</span></span> | <span data-ttu-id="d4ffb-125">Hull</span><span class="sxs-lookup"><span data-stu-id="d4ffb-125">Hull</span></span> | <span data-ttu-id="d4ffb-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="d4ffb-126">Domain</span></span> | <span data-ttu-id="d4ffb-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="d4ffb-127">Geometry</span></span> | <span data-ttu-id="d4ffb-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="d4ffb-128">Pixel</span></span> | <span data-ttu-id="d4ffb-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d4ffb-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d4ffb-130">x</span><span class="sxs-lookup"><span data-stu-id="d4ffb-130">x</span></span>     | <span data-ttu-id="d4ffb-131">x</span><span class="sxs-lookup"><span data-stu-id="d4ffb-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d4ffb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4ffb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ffb-133">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="d4ffb-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 