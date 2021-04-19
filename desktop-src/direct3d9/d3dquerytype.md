---
description: Identifica il tipo di query.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumerazione D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322918"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="d61c2-103">Enumerazione D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="d61c2-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="d61c2-104">Identifica il tipo di query.</span><span class="sxs-lookup"><span data-stu-id="d61c2-104">Identifies the query type.</span></span> <span data-ttu-id="d61c2-105">Per informazioni sulle query, vedere [query (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="d61c2-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="d61c2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d61c2-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="d61c2-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="d61c2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d61c2-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**\_VCACHE D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-109">Query per gli hint driver sul layout dei dati per la memorizzazione nella cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="d61c2-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**\_RESOURCEMANAGER D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-111">Eseguire una query in Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d61c2-111">Query the resource manager.</span></span> <span data-ttu-id="d61c2-112">Per questa query, i flag di comportamento del dispositivo devono includere [D3DCREATE \_ Disable \_ driver \_ Management](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="d61c2-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**\_VERTEXSTATS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-114">Eseguire query sulle statistiche del vertice.</span><span class="sxs-lookup"><span data-stu-id="d61c2-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Evento D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-116">Eseguire una query per tutti gli eventi asincroni emessi dalle chiamate API.</span><span class="sxs-lookup"><span data-stu-id="d61c2-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**\_Occlusione D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-118">Una query di occlusione restituisce il numero di pixel che superano il test z.</span><span class="sxs-lookup"><span data-stu-id="d61c2-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="d61c2-119">Questi pixel sono per le primitive tracciate tra il problema di [**D3DISSUE \_ Begin**](d3dissue-begin.md) e [**D3DISSUE \_ end**](d3dissue-end.md).</span><span class="sxs-lookup"><span data-stu-id="d61c2-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="d61c2-120">Questo consente a un'applicazione di verificare il risultato dell'occlusione rispetto a 0.</span><span class="sxs-lookup"><span data-stu-id="d61c2-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="d61c2-121">Zero è completamente nascosto, il che significa che i pixel non sono visibili dalla posizione corrente della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="d61c2-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Timestamp D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-123">Restituisce un timestamp a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d61c2-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**\_TIMESTAMPDISJOINT D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-125">Usare questa query per notificare a un'applicazione se la frequenza del contatore è cambiata rispetto al \_ timestamp D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="d61c2-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**\_TIMESTAMPFREQ D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-127">Il risultato della query è **true** se \_ non è possibile garantire che i valori delle query timestamp D3DQUERYTYPE siano continui per tutta la durata della \_ query TIMESTAMPDISJOINT D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="d61c2-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="d61c2-128">In caso contrario, il risultato della query è **false**.</span><span class="sxs-lookup"><span data-stu-id="d61c2-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**\_PIPELINETIMINGS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-130">Percentuale del tempo di elaborazione dei dati della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d61c2-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**\_INTERFACETIMINGS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-132">Percentuale del tempo di elaborazione dei dati nel driver.</span><span class="sxs-lookup"><span data-stu-id="d61c2-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**\_VERTEXTIMINGS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-134">Percentuale del tempo di elaborazione dei dati del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="d61c2-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**\_PIXELTIMINGS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-136">Percentuale del tempo di elaborazione dei dati pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d61c2-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**\_BANDWIDTHTIMINGS D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-138">Confronti di misurazione della velocità effettiva per aiutare a comprendere le prestazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d61c2-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**\_CACHEUTILIZATION D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-140">Misura le prestazioni della frequenza di riscontri nella cache per le trame e i vertici indicizzati.</span><span class="sxs-lookup"><span data-stu-id="d61c2-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d61c2-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**\_MEMORYPRESSURE D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d61c2-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="d61c2-142">Efficienza dell'allocazione di memoria contenuta in una struttura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="d61c2-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d61c2-143">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="d61c2-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="d61c2-144">D3DQUERYTYPE \_ MEMORYPRESSURE è disponibile solo in Direct3D9Ex in esecuzione su Windows 7 (o più sistemi operativi correnti).</span><span class="sxs-lookup"><span data-stu-id="d61c2-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d61c2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d61c2-145">Requirements</span></span>



| <span data-ttu-id="d61c2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d61c2-146">Requirement</span></span> | <span data-ttu-id="d61c2-147">Valore</span><span class="sxs-lookup"><span data-stu-id="d61c2-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d61c2-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d61c2-148">Header</span></span><br/> | <dl> <span data-ttu-id="d61c2-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d61c2-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61c2-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d61c2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61c2-151">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="d61c2-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d61c2-152">**IDirect3DDevice9:: CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="d61c2-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
