---
title: StructuredBuffer
description: Buffer di sola lettura che può assumere un tipo T che è una struttura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993408"
---
# <a name="structuredbuffer"></a><span data-ttu-id="34998-104">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="34998-104">StructuredBuffer</span></span>

<span data-ttu-id="34998-105">Buffer di sola lettura che può assumere un tipo T che è una struttura.</span><span class="sxs-lookup"><span data-stu-id="34998-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="34998-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="34998-106">Method</span></span>                                                             | <span data-ttu-id="34998-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34998-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="34998-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="34998-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="34998-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34998-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="34998-110">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="34998-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="34998-111">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="34998-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="34998-112">[**Operatore\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="34998-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="34998-113">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="34998-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="34998-114">Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="34998-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="34998-115">Per ulteriori informazioni sui [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), vedere il materiale di panoramica.</span><span class="sxs-lookup"><span data-stu-id="34998-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="34998-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="34998-116">Minimum Shader Model</span></span>

<span data-ttu-id="34998-117">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="34998-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="34998-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="34998-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="34998-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="34998-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="34998-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile per il calcolo e i pixel shader in Direct3D 11 su alcuni dispositivi Direct3D 10).</span><span class="sxs-lookup"><span data-stu-id="34998-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="34998-121">sì</span><span class="sxs-lookup"><span data-stu-id="34998-121">yes</span></span>       |



 

<span data-ttu-id="34998-122">Questo oggetto è supportato per i tipi di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="34998-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="34998-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="34998-123">Vertex</span></span> | <span data-ttu-id="34998-124">Hull</span><span class="sxs-lookup"><span data-stu-id="34998-124">Hull</span></span> | <span data-ttu-id="34998-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="34998-125">Domain</span></span> | <span data-ttu-id="34998-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="34998-126">Geometry</span></span> | <span data-ttu-id="34998-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="34998-127">Pixel</span></span> | <span data-ttu-id="34998-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="34998-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="34998-129">x</span><span class="sxs-lookup"><span data-stu-id="34998-129">x</span></span>      | <span data-ttu-id="34998-130">x</span><span class="sxs-lookup"><span data-stu-id="34998-130">x</span></span>    | <span data-ttu-id="34998-131">x</span><span class="sxs-lookup"><span data-stu-id="34998-131">x</span></span>      | <span data-ttu-id="34998-132">x</span><span class="sxs-lookup"><span data-stu-id="34998-132">x</span></span>        | <span data-ttu-id="34998-133">x</span><span class="sxs-lookup"><span data-stu-id="34998-133">x</span></span>     | <span data-ttu-id="34998-134">x</span><span class="sxs-lookup"><span data-stu-id="34998-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="34998-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34998-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34998-136">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="34998-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

