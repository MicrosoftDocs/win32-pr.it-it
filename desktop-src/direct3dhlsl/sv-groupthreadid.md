---
title: SV_GroupThreadID
description: Indici per cui un singolo thread all'interno di un gruppo di thread esegue uno shader di calcolo.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827030"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="e2212-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="e2212-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="e2212-105">Indici per cui un singolo thread all'interno di un gruppo di thread esegue uno shader di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e2212-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="e2212-106">SV \_ GroupThreadID varia in base all'intervallo specificato per lo shader di calcolo [nell'attributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="e2212-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="e2212-107">Se, ad esempio, numthreads(3,2,1) è stato specificato, i valori possibili per il valore di input SV GroupThreadID hanno questo intervallo di valori \_ (0-2,0-1,0).</span><span class="sxs-lookup"><span data-stu-id="e2212-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="e2212-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2212-108">Type</span></span>



| <span data-ttu-id="e2212-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2212-109">Type</span></span>      |
|-------|
| <span data-ttu-id="e2212-110">uint3</span><span class="sxs-lookup"><span data-stu-id="e2212-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2212-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2212-111">Remarks</span></span>

<span data-ttu-id="e2212-112">Questo valore di sistema è facoltativo ed è sempre compreso nei limiti dei valori passati [nell'attributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="e2212-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="e2212-113">La figura seguente illustra la relazione tra i parametri passati a [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati al thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)SV \_ GroupThreadID,[SV \_ GroupID).](sv-groupid.md)</span><span class="sxs-lookup"><span data-stu-id="e2212-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![Illustrazione della relazione tra dispatch, gruppi di thread e thread](images/threadgroupids.png)

<span data-ttu-id="e2212-115">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2212-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e2212-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="e2212-116">Vertex</span></span> | <span data-ttu-id="e2212-117">Scafo</span><span class="sxs-lookup"><span data-stu-id="e2212-117">Hull</span></span> | <span data-ttu-id="e2212-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="e2212-118">Domain</span></span> | <span data-ttu-id="e2212-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="e2212-119">Geometry</span></span> | <span data-ttu-id="e2212-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="e2212-120">Pixel</span></span> | <span data-ttu-id="e2212-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e2212-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="e2212-122">x</span><span class="sxs-lookup"><span data-stu-id="e2212-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e2212-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2212-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2212-124">Semantica</span><span class="sxs-lookup"><span data-stu-id="e2212-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="e2212-125">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="e2212-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
