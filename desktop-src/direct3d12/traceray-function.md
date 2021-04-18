---
description: Invia un raggio in una ricerca di riscontri in una struttura di accelerazione.
ms.assetid: ''
title: TraceRay (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320821"
---
# <a name="traceray-function"></a><span data-ttu-id="4df5f-103">TraceRay (funzione)</span><span class="sxs-lookup"><span data-stu-id="4df5f-103">TraceRay function</span></span>

<span data-ttu-id="4df5f-104">Invia un raggio in una ricerca di riscontri in una struttura di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="4df5f-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4df5f-105">Syntax</span></span>
<span data-ttu-id="4df5f-106">Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="4df5f-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="4df5f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4df5f-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="4df5f-108">Struttura di accelerazione di primo livello da usare.</span><span class="sxs-lookup"><span data-stu-id="4df5f-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="4df5f-109">La definizione di una struttura di accelerazione NULL impone un mancato riscontro.</span><span class="sxs-lookup"><span data-stu-id="4df5f-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="4df5f-110">Combinazione valida di valori di [ray_flag](ray_flag.md) .</span><span class="sxs-lookup"><span data-stu-id="4df5f-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="4df5f-111">Solo i flag raggio definiti vengono propagati dal sistema, ovvero sono visibili alla funzione intrinseca shader [RayFlags](rayflags.md) .</span><span class="sxs-lookup"><span data-stu-id="4df5f-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="4df5f-112">Un Unsigned Integer, gli 8 bit ultimi, usati per includere o rifiutare istanze geometry basate su InstanceMask in ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="4df5f-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="4df5f-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4df5f-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="4df5f-114">Unsigned Integer che specifica l'offset da aggiungere ai calcoli di indirizzamento nelle tabelle dello shader per l'indicizzazione del gruppo di hit.</span><span class="sxs-lookup"><span data-stu-id="4df5f-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="4df5f-115">Vengono utilizzati solo i 4 bit inferiori di questo valore.</span><span class="sxs-lookup"><span data-stu-id="4df5f-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="4df5f-116">Un Unsigned Integer che specifica lo stride da moltiplicare per *GeometryContributionToHitGroupIndex*, che è solo l'indice in base 0, che la geometria è stata fornita dall'app nella struttura di accelerazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="4df5f-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="4df5f-117">Vengono utilizzati solo i 16 bit inferiori del valore del moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="4df5f-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="4df5f-118">Unsigned Integer che specifica l'indice dello shader di mancato utilizzo in una tabella shader.</span><span class="sxs-lookup"><span data-stu-id="4df5f-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="4df5f-119">Oggetto [**RayDesc**](raydesc.md) che rappresenta il raggio da tracciare.</span><span class="sxs-lookup"><span data-stu-id="4df5f-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="4df5f-120">Payload con raggio definito dall'utente a cui si accede sia per l'input che per l'output da shader richiamati durante raytracing.</span><span class="sxs-lookup"><span data-stu-id="4df5f-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="4df5f-121">Al termine dell'esecuzione di [**TraceRay**](traceray-function.md) , il chiamante può accedere anche al payload.</span><span class="sxs-lookup"><span data-stu-id="4df5f-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="4df5f-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4df5f-122">Return Value</span></span>

<span data-ttu-id="4df5f-123">**void**</span><span class="sxs-lookup"><span data-stu-id="4df5f-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="4df5f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4df5f-124">Remarks</span></span>

<span data-ttu-id="4df5f-125">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="4df5f-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="4df5f-126">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="4df5f-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="4df5f-127">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="4df5f-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="4df5f-128">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="4df5f-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="4df5f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df5f-130">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="4df5f-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




