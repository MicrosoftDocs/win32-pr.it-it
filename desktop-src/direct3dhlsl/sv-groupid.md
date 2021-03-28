---
title: SV_GroupID
description: Indici per il gruppo di thread in cui è in esecuzione compute shader.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117898"
---
# <a name="sv_groupid"></a><span data-ttu-id="86ffc-104">\_GROUPID SV</span><span class="sxs-lookup"><span data-stu-id="86ffc-104">SV\_GroupID</span></span>

<span data-ttu-id="86ffc-105">Indici per il gruppo di thread in cui è in esecuzione compute shader.</span><span class="sxs-lookup"><span data-stu-id="86ffc-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="86ffc-106">Gli indici sono per l'intero gruppo e non per un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="86ffc-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="86ffc-107">I valori possibili variano nell'intervallo passato come parametri da [**inviare**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="86ffc-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="86ffc-108">Se ad esempio si chiama dispatch (2, 1, 1), i valori possibili sono 0, 0, 0 e 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="86ffc-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="86ffc-109">Definisce l'offset di gruppo all'interno di una chiamata di [**invio**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , per dimensione della chiamata di invio.</span><span class="sxs-lookup"><span data-stu-id="86ffc-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="86ffc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="86ffc-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="86ffc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="86ffc-111">Type</span></span>  |
| <span data-ttu-id="86ffc-112">uint3</span><span class="sxs-lookup"><span data-stu-id="86ffc-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="86ffc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="86ffc-113">Remarks</span></span>

<span data-ttu-id="86ffc-114">Questo valore di sistema è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="86ffc-114">This system value is optional.</span></span>

<span data-ttu-id="86ffc-115">Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).</span><span class="sxs-lookup"><span data-stu-id="86ffc-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

<span data-ttu-id="86ffc-117">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="86ffc-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="86ffc-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="86ffc-118">Vertex</span></span> | <span data-ttu-id="86ffc-119">Hull</span><span class="sxs-lookup"><span data-stu-id="86ffc-119">Hull</span></span> | <span data-ttu-id="86ffc-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="86ffc-120">Domain</span></span> | <span data-ttu-id="86ffc-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="86ffc-121">Geometry</span></span> | <span data-ttu-id="86ffc-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="86ffc-122">Pixel</span></span> | <span data-ttu-id="86ffc-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="86ffc-123">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="86ffc-124">x</span><span class="sxs-lookup"><span data-stu-id="86ffc-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="86ffc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86ffc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ffc-126">Semantica</span><span class="sxs-lookup"><span data-stu-id="86ffc-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="86ffc-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="86ffc-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 