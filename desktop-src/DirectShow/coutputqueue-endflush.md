---
description: "Metodo COutputQueue.EndFlush: il metodo EndFlush termina un'operazione di scaricamento."
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Metodo COutputQueue.EndFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099009"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="94de4-103">Metodo COutputQueue.EndFlush</span><span class="sxs-lookup"><span data-stu-id="94de4-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="94de4-104">Il `EndFlush` metodo termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="94de4-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="94de4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94de4-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="94de4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94de4-106">Parameters</span></span>

<span data-ttu-id="94de4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="94de4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94de4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94de4-108">Return value</span></span>

<span data-ttu-id="94de4-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="94de4-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94de4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="94de4-110">Remarks</span></span>

<span data-ttu-id="94de4-111">Se l'oggetto usa un thread, questo metodo attende l'evento [**COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="94de4-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="94de4-112">Il thread segnala questo evento dopo aver liberato eventuali campioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="94de4-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="94de4-113">Se l'oggetto non usa un thread, questo metodo chiama il [**metodo COutputQueue::FreeSamples.**](coutputqueue-freesamples.md)</span><span class="sxs-lookup"><span data-stu-id="94de4-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="94de4-114">Il metodo `EndFlush` chiama quindi il metodo [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="94de4-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="94de4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94de4-115">Requirements</span></span>



| <span data-ttu-id="94de4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="94de4-116">Requirement</span></span> | <span data-ttu-id="94de4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="94de4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94de4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94de4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="94de4-119"><dt>Outputq.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="94de4-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94de4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="94de4-120">Library</span></span><br/> | <dl> <span data-ttu-id="94de4-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="94de4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94de4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94de4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94de4-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="94de4-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




