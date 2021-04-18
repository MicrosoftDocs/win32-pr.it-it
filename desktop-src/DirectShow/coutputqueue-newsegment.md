---
description: Il metodo NewSegment recapita un nuovo segmento al pin di input.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Metodo COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329521"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="7e941-103">COutputQueue. NewSegment, metodo</span><span class="sxs-lookup"><span data-stu-id="7e941-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="7e941-104">Il `NewSegment` Metodo recapita un nuovo segmento al pin di input.</span><span class="sxs-lookup"><span data-stu-id="7e941-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e941-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e941-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="7e941-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e941-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="7e941-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="7e941-108">Posizione iniziale del supporto del segmento, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="7e941-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="7e941-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="7e941-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="7e941-110">Posizione media finale del segmento, in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="7e941-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="7e941-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="7e941-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="7e941-112">Velocità di elaborazione del segmento, espresso come percentuale della frequenza originale.</span><span class="sxs-lookup"><span data-stu-id="7e941-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e941-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e941-113">Return value</span></span>

<span data-ttu-id="7e941-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e941-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e941-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e941-115">Remarks</span></span>

<span data-ttu-id="7e941-116">Se l'oggetto utilizza un thread, Accoda gli elementi seguenti in ordine:</span><span class="sxs-lookup"><span data-stu-id="7e941-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="7e941-117">NUOVO \_ messaggio di controllo del segmento.</span><span class="sxs-lookup"><span data-stu-id="7e941-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="7e941-118">Dati del segmento.</span><span class="sxs-lookup"><span data-stu-id="7e941-118">The segment data.</span></span>

<span data-ttu-id="7e941-119">Il \_ messaggio nuovo segmento notifica al thread che l'elemento successivo nella coda conterrà i dati del segmento.</span><span class="sxs-lookup"><span data-stu-id="7e941-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="7e941-120">I dati del segmento vengono aggregati in una struttura, dichiarati come segue:</span><span class="sxs-lookup"><span data-stu-id="7e941-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="7e941-121">Il thread chiama il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input, usando i dati forniti nella struttura.</span><span class="sxs-lookup"><span data-stu-id="7e941-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="7e941-122">Se l'oggetto non utilizza un thread, viene chiamato il metodo [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7e941-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="7e941-123">Chiama quindi **Ipin:: NewSegment** sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="7e941-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e941-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e941-124">Requirements</span></span>



| <span data-ttu-id="7e941-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e941-125">Requirement</span></span> | <span data-ttu-id="7e941-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7e941-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e941-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e941-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7e941-128"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e941-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7e941-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e941-129">Library</span></span><br/> | <dl> <span data-ttu-id="7e941-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7e941-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e941-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e941-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e941-132">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="7e941-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




