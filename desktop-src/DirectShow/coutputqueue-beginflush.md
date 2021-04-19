---
description: Il Metodo BeginFlush avvia un'operazione di svuotamento.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Metodo COutputQueue. BeginFlush (Outputq. h)
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
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330214"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="3573d-103">COutputQueue. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="3573d-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="3573d-104">Il `BeginFlush` metodo inizia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="3573d-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3573d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3573d-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="3573d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3573d-106">Parameters</span></span>

<span data-ttu-id="3573d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3573d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3573d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3573d-108">Return value</span></span>

<span data-ttu-id="3573d-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3573d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3573d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3573d-110">Remarks</span></span>

<span data-ttu-id="3573d-111">Questo metodo imposta la variabile membro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="3573d-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="3573d-112">Se l'oggetto utilizza un thread, il thread chiama il metodo [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) per liberare tutti gli esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="3573d-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="3573d-113">In caso contrario, l'oggetto chiama **FreeSamples** durante il metodo [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="3573d-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="3573d-114">Questo metodo imposta anche la variabile membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) su S \_ false, che fa sì che l'oggetto elimini tutti i nuovi esempi.</span><span class="sxs-lookup"><span data-stu-id="3573d-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="3573d-115">L'oggetto passa la notifica di scaricamento downstream chiamando il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="3573d-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3573d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3573d-116">Requirements</span></span>



| <span data-ttu-id="3573d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3573d-117">Requirement</span></span> | <span data-ttu-id="3573d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3573d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3573d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3573d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3573d-120"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3573d-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3573d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3573d-121">Library</span></span><br/> | <dl> <span data-ttu-id="3573d-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3573d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3573d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3573d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3573d-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="3573d-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




