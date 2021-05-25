---
description: Identifica il tipo di query.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumerazione D3DQUERYTYPE (D3D9Types.h)
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
ms.openlocfilehash: 7a9c20050e7d0dce5a19664d937c016a475a9a13
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343076"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="a60ea-103">Enumerazione D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="a60ea-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="a60ea-104">Identifica il tipo di query.</span><span class="sxs-lookup"><span data-stu-id="a60ea-104">Identifies the query type.</span></span> <span data-ttu-id="a60ea-105">Per informazioni sulle query, vedere [Query (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="a60ea-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="a60ea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a60ea-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="a60ea-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="a60ea-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a60ea-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="a60ea-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-109">Query per gli hint del driver sul layout dei dati per la memorizzazione nella cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="a60ea-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="a60ea-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-111">Eseguire query sul gestore di risorse.</span><span class="sxs-lookup"><span data-stu-id="a60ea-111">Query the resource manager.</span></span> <span data-ttu-id="a60ea-112">Per questa query, i flag di comportamento del dispositivo devono includere [D3DCREATE \_ DISABLE \_ DRIVER \_ MANAGEMENT](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="a60ea-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="a60ea-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-114">Eseguire query sulle statistiche dei vertici.</span><span class="sxs-lookup"><span data-stu-id="a60ea-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**EVENTO D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="a60ea-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-116">Eseguire una query per tutti gli eventi asincroni emessi dalle chiamate API.</span><span class="sxs-lookup"><span data-stu-id="a60ea-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**OCCLUSIONE D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="a60ea-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-118">Una query di occlusione restituisce il numero di pixel che superano z-testing.</span><span class="sxs-lookup"><span data-stu-id="a60ea-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="a60ea-119">Questi pixel sono per le primitive disegnate tra il problema [**di D3DISSUE \_ BEGIN**](d3dissue-begin.md) e [**D3DISSUE \_ END.**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="a60ea-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="a60ea-120">In questo modo un'applicazione può controllare il risultato dell'occlusione rispetto a 0.</span><span class="sxs-lookup"><span data-stu-id="a60ea-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="a60ea-121">Zero è completamente occluso, ovvero i pixel non sono visibili dalla posizione corrente della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="a60ea-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ TIMESTAMP**</span><span class="sxs-lookup"><span data-stu-id="a60ea-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-123">Restituisce un timestamp a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a60ea-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**TIMESTAMP \_ D3DQUERYTYPEDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="a60ea-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-125">Usare questa query per inviare una notifica a un'applicazione se la frequenza del contatore è stata modificata rispetto a D3DQUERYTYPE \_ TIMESTAMP.</span><span class="sxs-lookup"><span data-stu-id="a60ea-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**TIMESTAMP D3DQUERYTYPEFREQ \_**</span><span class="sxs-lookup"><span data-stu-id="a60ea-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-127">Questo risultato della query è **TRUE** se non è possibile garantire che i valori delle query TIMESTAMP D3DQUERYTYPE siano continui per tutta la durata della \_ query D3DQUERYTYPE \_ TIMESTAMPDISJOINT.</span><span class="sxs-lookup"><span data-stu-id="a60ea-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="a60ea-128">In caso contrario, il risultato della query è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a60ea-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**\_PIPELINE D3DQUERYTYPETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="a60ea-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-130">Percentuale di tempo di elaborazione dei dati della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a60ea-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**INTERFACCIA \_ D3DQUERYTYPETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="a60ea-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-132">Percentuale di tempo di elaborazione dei dati nel driver.</span><span class="sxs-lookup"><span data-stu-id="a60ea-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="a60ea-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-134">Percentuale di tempo di elaborazione dei dati vertex shader.</span><span class="sxs-lookup"><span data-stu-id="a60ea-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**PIXELTIMING D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="a60ea-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-136">Percentuale di tempo di elaborazione pixel shader dati.</span><span class="sxs-lookup"><span data-stu-id="a60ea-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="a60ea-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-138">Confronti delle misurazioni della velocità effettiva per comprendere le prestazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a60ea-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="a60ea-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-140">Misurare le prestazioni di hit rate della cache per trame e vertici indicizzati.</span><span class="sxs-lookup"><span data-stu-id="a60ea-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a60ea-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="a60ea-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="a60ea-142">Efficienza dell'allocazione di memoria contenuta in [**una struttura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)</span><span class="sxs-lookup"><span data-stu-id="a60ea-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="a60ea-143">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a60ea-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="a60ea-144">D3DQUERYTYPE MEMORYPRESSURE è disponibile solo \_ in Direct3D9Ex in esecuzione in Windows 7 (o in un sistema operativo più corrente).</span><span class="sxs-lookup"><span data-stu-id="a60ea-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a60ea-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a60ea-145">Requirements</span></span>



| <span data-ttu-id="a60ea-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a60ea-146">Requirement</span></span> | <span data-ttu-id="a60ea-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a60ea-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a60ea-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a60ea-148">Header</span></span><br/> | <dl> <span data-ttu-id="a60ea-149"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="a60ea-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a60ea-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a60ea-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60ea-151">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="a60ea-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a60ea-152">**IDirect3DDevice9::CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="a60ea-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
