---
description: Puntatore a una sezione critica utilizzata per serializzare le modifiche di stato.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membro CBaseFilter:: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327219"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="83b91-103">Membro pLock di CBaseFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="83b91-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="83b91-104">Puntatore a una sezione critica utilizzata per serializzare le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="83b91-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83b91-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="83b91-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="83b91-106">Remarks</span></span>

<span data-ttu-id="83b91-107">Questa variabile viene inizializzata nel costruttore della classe; vedere [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="83b91-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="83b91-108">Questa sezione critica viene mantenuta durante le transizioni di stato o quando un metodo accede allo stato su più operazioni.</span><span class="sxs-lookup"><span data-stu-id="83b91-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="83b91-109">La classe base include la sezione Critical nei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b91-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="83b91-110">**CBaseFilter::FindPin**</span><span class="sxs-lookup"><span data-stu-id="83b91-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="83b91-111">**CBaseFilter::GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="83b91-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="83b91-112">**CBaseFilter::JoinFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="83b91-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="83b91-113">**CBaseFilter:: inattivo**</span><span class="sxs-lookup"><span data-stu-id="83b91-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="83b91-114">**CBaseFilter::SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="83b91-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="83b91-115">**CBaseFilter::P ause**</span><span class="sxs-lookup"><span data-stu-id="83b91-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="83b91-116">**CBaseFilter:: Run**</span><span class="sxs-lookup"><span data-stu-id="83b91-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="83b91-117">**CBaseFilter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="83b91-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="83b91-118">Non mantenere questa sezione critica durante le operazioni di streaming, ovvero durante la distribuzione di campioni a un filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="83b91-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="83b91-119">Serializzare le operazioni di streaming usando un'altra sezione critica.</span><span class="sxs-lookup"><span data-stu-id="83b91-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="83b91-120">In caso contrario, può causare un deadlock.</span><span class="sxs-lookup"><span data-stu-id="83b91-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b91-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83b91-121">Requirements</span></span>



| <span data-ttu-id="83b91-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b91-122">Requirement</span></span> | <span data-ttu-id="83b91-123">Valore</span><span class="sxs-lookup"><span data-stu-id="83b91-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b91-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83b91-124">Header</span></span><br/>  | <dl> <span data-ttu-id="83b91-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83b91-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="83b91-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="83b91-126">Library</span></span><br/> | <dl> <span data-ttu-id="83b91-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="83b91-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b91-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83b91-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b91-129">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="83b91-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="83b91-130">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="83b91-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




