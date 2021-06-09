---
title: SV_DispatchThreadID
description: Indici per i quali un thread e un gruppo di thread combinati eseguono uno shader di calcolo.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e2713aaa50206660f7672688a43e644873b1c13
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827060"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="561ac-104">SV \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="561ac-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="561ac-105">Indici per i quali un thread e un gruppo di thread combinati eseguono uno shader di calcolo.</span><span class="sxs-lookup"><span data-stu-id="561ac-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="561ac-106">SV \_ DispatchThreadID è la somma di \_ SV GroupID \* numthreads e GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="561ac-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="561ac-107">Varia in base all'intervallo specificato in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="561ac-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="561ac-108">Ad esempio, se Dispatch(2,2,2) viene chiamato in un compute shader con numthreads(3,3,3) SV \_ DispatchThreadID avrà un intervallo di 0,.5 per ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="561ac-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="561ac-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="561ac-109">Type</span></span>



| <span data-ttu-id="561ac-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="561ac-110">Type</span></span>      |
|-------|
| <span data-ttu-id="561ac-111">uint3</span><span class="sxs-lookup"><span data-stu-id="561ac-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="561ac-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="561ac-112">Remarks</span></span>

<span data-ttu-id="561ac-113">Questo valore di sistema è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="561ac-113">This system value is optional.</span></span>

<span data-ttu-id="561ac-114">La figura seguente illustra la relazione tra i parametri passati a [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati al thread ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="561ac-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Illustrazione della relazione tra dispatch, gruppi di thread e thread](images/threadgroupids.png)

<span data-ttu-id="561ac-116">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="561ac-116">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="561ac-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="561ac-117">Vertex</span></span> | <span data-ttu-id="561ac-118">Scafo</span><span class="sxs-lookup"><span data-stu-id="561ac-118">Hull</span></span> | <span data-ttu-id="561ac-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="561ac-119">Domain</span></span> | <span data-ttu-id="561ac-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="561ac-120">Geometry</span></span> | <span data-ttu-id="561ac-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="561ac-121">Pixel</span></span> | <span data-ttu-id="561ac-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="561ac-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="561ac-123">x</span><span class="sxs-lookup"><span data-stu-id="561ac-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="561ac-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="561ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561ac-125">Semantica</span><span class="sxs-lookup"><span data-stu-id="561ac-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="561ac-126">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="561ac-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
