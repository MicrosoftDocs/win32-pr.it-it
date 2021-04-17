---
title: SV_GroupThreadID
description: Indici per cui è in esecuzione un singolo thread in un gruppo di thread in cui è in esecuzione compute shader.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338983"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="e7844-104">\_GROUPTHREADID SV</span><span class="sxs-lookup"><span data-stu-id="e7844-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="e7844-105">Indici per cui è in esecuzione un singolo thread in un gruppo di thread in cui è in esecuzione compute shader.</span><span class="sxs-lookup"><span data-stu-id="e7844-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="e7844-106">SV \_ GroupThreadID varia in base all'intervallo specificato per compute shader nell'attributo [numThreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="e7844-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="e7844-107">Se, ad esempio, numThreads (3, 2, 1) è stato specificato, i valori possibili per il \_ valore di input SV GroupThreadID includono questo intervallo di valori (0-2, 0-1, 0).</span><span class="sxs-lookup"><span data-stu-id="e7844-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="e7844-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7844-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="e7844-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7844-109">Type</span></span>  |
| <span data-ttu-id="e7844-110">uint3</span><span class="sxs-lookup"><span data-stu-id="e7844-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e7844-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7844-111">Remarks</span></span>

<span data-ttu-id="e7844-112">Questo valore di sistema è facoltativo ed è sempre compreso tra i limiti dei valori passati nell'attributo [numThreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="e7844-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="e7844-113">Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="e7844-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

<span data-ttu-id="e7844-115">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7844-115">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e7844-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="e7844-116">Vertex</span></span> | <span data-ttu-id="e7844-117">Hull</span><span class="sxs-lookup"><span data-stu-id="e7844-117">Hull</span></span> | <span data-ttu-id="e7844-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="e7844-118">Domain</span></span> | <span data-ttu-id="e7844-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="e7844-119">Geometry</span></span> | <span data-ttu-id="e7844-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="e7844-120">Pixel</span></span> | <span data-ttu-id="e7844-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e7844-121">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="e7844-122">x</span><span class="sxs-lookup"><span data-stu-id="e7844-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e7844-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7844-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7844-124">Semantica</span><span class="sxs-lookup"><span data-stu-id="e7844-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="e7844-125">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e7844-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 