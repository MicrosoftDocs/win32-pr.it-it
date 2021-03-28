---
title: RWStructuredBuffer
description: Un buffer di lettura/scrittura che può assumere un tipo T che è una struttura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL RWStructuredBuffer
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399205"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="38421-104">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="38421-104">RWStructuredBuffer</span></span>

<span data-ttu-id="38421-105">Un buffer di lettura/scrittura che può assumere un tipo T che è una struttura.</span><span class="sxs-lookup"><span data-stu-id="38421-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="38421-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="38421-106">Method</span></span>                                                                     | <span data-ttu-id="38421-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38421-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="38421-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="38421-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="38421-109">Decrementa il contatore nascosto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38421-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="38421-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="38421-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="38421-111">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="38421-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="38421-112">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="38421-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="38421-113">Incrementa il contatore nascosto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38421-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="38421-114">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="38421-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="38421-115">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="38421-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="38421-116">[**Operatore\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="38421-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="38421-117">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="38421-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="38421-118">Una variabile di risorsa può essere passata anche in qualsiasi operazione non ordinata o Interlocked.</span><span class="sxs-lookup"><span data-stu-id="38421-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="38421-119">Gli oggetti RWStructuredBuffer possono essere preceduti dalla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="38421-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="38421-120">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="38421-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="38421-121">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica solo un UAV all'interno del gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="38421-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="38421-122">Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="38421-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="38421-123">Per ulteriori informazioni sui [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), vedere il materiale di panoramica.</span><span class="sxs-lookup"><span data-stu-id="38421-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="38421-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="38421-124">Minimum Shader Model</span></span>

<span data-ttu-id="38421-125">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="38421-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="38421-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="38421-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="38421-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="38421-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="38421-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader.</span><span class="sxs-lookup"><span data-stu-id="38421-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="38421-129">Per ulteriori informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="38421-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="38421-130">sì</span><span class="sxs-lookup"><span data-stu-id="38421-130">yes</span></span>       |



 

<span data-ttu-id="38421-131">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="38421-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="38421-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="38421-132">Vertex</span></span> | <span data-ttu-id="38421-133">Hull</span><span class="sxs-lookup"><span data-stu-id="38421-133">Hull</span></span> | <span data-ttu-id="38421-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="38421-134">Domain</span></span> | <span data-ttu-id="38421-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="38421-135">Geometry</span></span> | <span data-ttu-id="38421-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="38421-136">Pixel</span></span> | <span data-ttu-id="38421-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="38421-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="38421-138">x</span><span class="sxs-lookup"><span data-stu-id="38421-138">x</span></span>     | <span data-ttu-id="38421-139">x</span><span class="sxs-lookup"><span data-stu-id="38421-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="38421-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38421-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38421-141">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="38421-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

