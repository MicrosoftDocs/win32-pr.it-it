---
description: Il metodo QueueSample accoda un esempio.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Metodo COutputQueue.QueueSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910069"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="43105-103">Metodo COutputQueue.QueueSample</span><span class="sxs-lookup"><span data-stu-id="43105-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="43105-104">Il `QueueSample` metodo accoda un esempio.</span><span class="sxs-lookup"><span data-stu-id="43105-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="43105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43105-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="43105-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43105-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="43105-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="43105-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="43105-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43105-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43105-109">Return value</span></span>

<span data-ttu-id="43105-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="43105-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43105-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="43105-111">Remarks</span></span>

<span data-ttu-id="43105-112">Questo metodo aggiunge un campione alla parte finale della coda.</span><span class="sxs-lookup"><span data-stu-id="43105-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="43105-113">Mantenere la sezione critica prima di chiamare questo metodo e chiamarla solo quando l'oggetto usa un thread per distribuire i campioni.</span><span class="sxs-lookup"><span data-stu-id="43105-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="43105-114">Per determinare se l'oggetto usa un thread, chiamare il [**metodo COutputQueue::IsQueued.**](coutputqueue-isqueued.md)</span><span class="sxs-lookup"><span data-stu-id="43105-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="43105-115">Questo metodo può essere usato anche per inserire i messaggi di controllo nella coda.</span><span class="sxs-lookup"><span data-stu-id="43105-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="43105-116">Un messaggio di controllo è una costante definita (cast a un tipo PTR LONG) che indica al \_ thread di eseguire un'azione.</span><span class="sxs-lookup"><span data-stu-id="43105-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="43105-117">La **classe COutputQueue** definisce i messaggi di controllo illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="43105-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="43105-118">Label</span><span class="sxs-lookup"><span data-stu-id="43105-118">Label</span></span> | <span data-ttu-id="43105-119">Valore</span><span class="sxs-lookup"><span data-stu-id="43105-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="43105-120">Message</span><span class="sxs-lookup"><span data-stu-id="43105-120">Message</span></span>       | <span data-ttu-id="43105-121">Azione</span><span class="sxs-lookup"><span data-stu-id="43105-121">Action</span></span>                                 |
| <span data-ttu-id="43105-122">PACCHETTO \_ EOS</span><span class="sxs-lookup"><span data-stu-id="43105-122">EOS\_PACKET</span></span>   | <span data-ttu-id="43105-123">Recapitare una notifica di fine flusso.</span><span class="sxs-lookup"><span data-stu-id="43105-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="43105-124">NUOVO \_ SEGMENTO</span><span class="sxs-lookup"><span data-stu-id="43105-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="43105-125">Distribuire un nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="43105-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="43105-126">REIMPOSTA \_ PACCHETTO</span><span class="sxs-lookup"><span data-stu-id="43105-126">RESET\_PACKET</span></span> | <span data-ttu-id="43105-127">Reimpostare lo stato della coda.</span><span class="sxs-lookup"><span data-stu-id="43105-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="43105-128">SEND \_ PACKET</span><span class="sxs-lookup"><span data-stu-id="43105-128">SEND\_PACKET</span></span>  | <span data-ttu-id="43105-129">Inviare un batch parziale di campioni.</span><span class="sxs-lookup"><span data-stu-id="43105-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="43105-130">Si tratta di un metodo protetto, che la **classe COutputQueue usa** internamente.</span><span class="sxs-lookup"><span data-stu-id="43105-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="43105-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43105-131">Requirements</span></span>



| <span data-ttu-id="43105-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="43105-132">Requirement</span></span> | <span data-ttu-id="43105-133">Valore</span><span class="sxs-lookup"><span data-stu-id="43105-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43105-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43105-134">Header</span></span><br/>  | <dl> <span data-ttu-id="43105-135"><dt>Outputq.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="43105-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43105-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="43105-136">Library</span></span><br/> | <dl> <span data-ttu-id="43105-137"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43105-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43105-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43105-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43105-139">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="43105-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




