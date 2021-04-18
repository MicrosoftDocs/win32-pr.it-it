---
title: SV_DispatchThreadID
description: Indici per i quali viene eseguito un compute shader in un gruppo di thread e thread combinato.
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
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104560326"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="a0748-104">\_DISPATCHTHREADID SV</span><span class="sxs-lookup"><span data-stu-id="a0748-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="a0748-105">Indici per i quali viene eseguito un compute shader in un gruppo di thread e thread combinato.</span><span class="sxs-lookup"><span data-stu-id="a0748-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="a0748-106">SV \_ DispatchThreadID è la somma di SV \_ GroupID \* numThreads e GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="a0748-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="a0748-107">Varia in base all'intervallo specificato in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numThreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="a0748-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="a0748-108">Ad esempio, se dispatch (2, 2, 2) viene chiamato in un compute shader con numThreads (3, 3, 3) SV \_ DispatchThreadID avrà un intervallo di 0.5 per ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="a0748-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="a0748-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0748-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="a0748-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0748-110">Type</span></span>  |
| <span data-ttu-id="a0748-111">uint3</span><span class="sxs-lookup"><span data-stu-id="a0748-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a0748-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0748-112">Remarks</span></span>

<span data-ttu-id="a0748-113">Questo valore di sistema è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0748-113">This system value is optional.</span></span>

<span data-ttu-id="a0748-114">Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="a0748-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

<span data-ttu-id="a0748-116">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0748-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0748-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="a0748-117">Vertex</span></span> | <span data-ttu-id="a0748-118">Hull</span><span class="sxs-lookup"><span data-stu-id="a0748-118">Hull</span></span> | <span data-ttu-id="a0748-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="a0748-119">Domain</span></span> | <span data-ttu-id="a0748-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="a0748-120">Geometry</span></span> | <span data-ttu-id="a0748-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="a0748-121">Pixel</span></span> | <span data-ttu-id="a0748-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a0748-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="a0748-123">x</span><span class="sxs-lookup"><span data-stu-id="a0748-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0748-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0748-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0748-125">Semantica</span><span class="sxs-lookup"><span data-stu-id="a0748-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="a0748-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a0748-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 