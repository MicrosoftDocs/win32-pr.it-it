---
description: "Metodo COutputQueue.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Metodo COutputQueue.BeginFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099029"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="9f16b-103">Metodo COutputQueue.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="9f16b-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="9f16b-104">Il `BeginFlush` metodo avvia un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="9f16b-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f16b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f16b-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="9f16b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f16b-106">Parameters</span></span>

<span data-ttu-id="9f16b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f16b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f16b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f16b-108">Return value</span></span>

<span data-ttu-id="9f16b-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9f16b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f16b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f16b-110">Remarks</span></span>

<span data-ttu-id="9f16b-111">Questo metodo imposta la [**variabile membro COutputQueue::m \_ bFlushing**](coutputqueue-m-bflushing.md) su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9f16b-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="9f16b-112">Se l'oggetto usa un thread, il thread chiama il metodo [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) per liberare eventuali esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9f16b-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="9f16b-113">In caso contrario, **l'oggetto chiama FreeSamples** durante [**il metodo COutputQueue::EndFlush.**](coutputqueue-endflush.md)</span><span class="sxs-lookup"><span data-stu-id="9f16b-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="9f16b-114">Questo metodo imposta anche la variabile membro [**COutputQueue::m \_ hr**](coutputqueue-m-hr.md) su S FALSE, in modo che l'oggetto scarti \_ tutti i nuovi esempi.</span><span class="sxs-lookup"><span data-stu-id="9f16b-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="9f16b-115">L'oggetto passa la notifica di scaricamento a valle chiamando il [**metodo IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="9f16b-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f16b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f16b-116">Requirements</span></span>



| <span data-ttu-id="9f16b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f16b-117">Requirement</span></span> | <span data-ttu-id="9f16b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9f16b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f16b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f16b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9f16b-120"><dt>Outputq.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f16b-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f16b-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f16b-121">Library</span></span><br/> | <dl> <span data-ttu-id="9f16b-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f16b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f16b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f16b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f16b-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="9f16b-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




