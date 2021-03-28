---
title: ConsumeStructuredBuffer
description: Un buffer di input che viene visualizzato come flusso da cui lo shader può effettuare il pull dei valori. Solo i buffer strutturati possono assumere tipi T che sono strutture.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993597"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="bb2d3-105">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="bb2d3-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="bb2d3-106">Un buffer di input che viene visualizzato come flusso da cui lo shader può effettuare il pull dei valori.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="bb2d3-107">Solo i buffer strutturati possono assumere tipi T che sono strutture.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="bb2d3-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="bb2d3-108">Method</span></span>                                                                    | <span data-ttu-id="bb2d3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb2d3-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="bb2d3-110">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="bb2d3-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="bb2d3-111">Rimuove un valore dalla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="bb2d3-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="bb2d3-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="bb2d3-113">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="bb2d3-114">Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="bb2d3-115">È necessario che l'UAV associato a questa risorsa sia stato creato con l' [**\_ \_ \_ \_ aggiunta del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="bb2d3-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="bb2d3-116">Per ulteriori informazioni sull'utilizzo dei buffer strutturati, vedere entrambe le sezioni: [Accodamento e utilizzo del buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e del [buffer strutturato](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="bb2d3-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bb2d3-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bb2d3-117">Minimum Shader Model</span></span>

<span data-ttu-id="bb2d3-118">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb2d3-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="bb2d3-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bb2d3-119">Shader Model</span></span>                                                                | <span data-ttu-id="bb2d3-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="bb2d3-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bb2d3-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="bb2d3-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bb2d3-122">sì</span><span class="sxs-lookup"><span data-stu-id="bb2d3-122">yes</span></span>       |



 

<span data-ttu-id="bb2d3-123">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb2d3-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bb2d3-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="bb2d3-124">Vertex</span></span> | <span data-ttu-id="bb2d3-125">Hull</span><span class="sxs-lookup"><span data-stu-id="bb2d3-125">Hull</span></span> | <span data-ttu-id="bb2d3-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="bb2d3-126">Domain</span></span> | <span data-ttu-id="bb2d3-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="bb2d3-127">Geometry</span></span> | <span data-ttu-id="bb2d3-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="bb2d3-128">Pixel</span></span> | <span data-ttu-id="bb2d3-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="bb2d3-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bb2d3-130">x</span><span class="sxs-lookup"><span data-stu-id="bb2d3-130">x</span></span>     | <span data-ttu-id="bb2d3-131">x</span><span class="sxs-lookup"><span data-stu-id="bb2d3-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bb2d3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb2d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2d3-133">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="bb2d3-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 