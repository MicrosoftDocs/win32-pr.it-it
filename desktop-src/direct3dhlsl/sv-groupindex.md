---
title: SV_GroupIndex
description: "\\ 0034; flatd \\ 0034; Indice di un thread compute shader all'interno di un gruppo di thread, che converte l'oggetto SV GroupThreadID multidimensionale \\_ in un valore 1D. SV \\_ groupIndex varia da 0 a (numthreadsX \\ numthreadsY \\ numThreadsZ) \\ 8211; 1."
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728178"
---
# <a name="sv_groupindex"></a><span data-ttu-id="15333-105">\_GROUPINDEX SV</span><span class="sxs-lookup"><span data-stu-id="15333-105">SV\_GroupIndex</span></span>

<span data-ttu-id="15333-106">Indice "flat" di un thread compute shader all'interno di un gruppo di thread, che trasforma l'oggetto SV \_ GroupThreadID multidimensionali in un valore 1D.</span><span class="sxs-lookup"><span data-stu-id="15333-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="15333-107">SV \_ groupIndex varia da 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span><span class="sxs-lookup"><span data-stu-id="15333-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="15333-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="15333-108">Type</span></span>



| <span data-ttu-id="15333-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="15333-109">Type</span></span> |
|------|
| <span data-ttu-id="15333-110">uint</span><span class="sxs-lookup"><span data-stu-id="15333-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="15333-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="15333-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="15333-112">dove dimx e Dimy sono le dimensioni specificate nell'attributo [numThreads](sm5-attributes-numthreads.md) per il punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="15333-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="15333-113">Questo valore di sistema è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="15333-113">This system value is optional.</span></span> <span data-ttu-id="15333-114">Tuttavia, il suo utilizzo garantisce che un thread scriva solo nell'area di memoria assegnata nella variabile groupshared.</span><span class="sxs-lookup"><span data-stu-id="15333-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="15333-115">Nella figura seguente viene illustrata la relazione tra i parametri passati a [**sul ID3D11DeviceContext::D di patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati al thread (SV \_ groupIndex,[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="15333-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

<span data-ttu-id="15333-117">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="15333-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="15333-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="15333-118">Vertex</span></span> | <span data-ttu-id="15333-119">Hull</span><span class="sxs-lookup"><span data-stu-id="15333-119">Hull</span></span> | <span data-ttu-id="15333-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="15333-120">Domain</span></span> | <span data-ttu-id="15333-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="15333-121">Geometry</span></span> | <span data-ttu-id="15333-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="15333-122">Pixel</span></span> | <span data-ttu-id="15333-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="15333-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="15333-124">x</span><span class="sxs-lookup"><span data-stu-id="15333-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15333-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15333-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15333-126">Semantica</span><span class="sxs-lookup"><span data-stu-id="15333-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="15333-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="15333-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 