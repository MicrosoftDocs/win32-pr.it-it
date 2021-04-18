---
description: Il metodo QueueSample Accoda un campione.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Metodo COutputQueue. QueueSample (Outputq. h)
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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324682"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="895d9-103">COutputQueue. QueueSample, metodo</span><span class="sxs-lookup"><span data-stu-id="895d9-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="895d9-104">Il `QueueSample` Metodo Accoda un campione.</span><span class="sxs-lookup"><span data-stu-id="895d9-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="895d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="895d9-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="895d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="895d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="895d9-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="895d9-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="895d9-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="895d9-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="895d9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="895d9-109">Return value</span></span>

<span data-ttu-id="895d9-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="895d9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="895d9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="895d9-111">Remarks</span></span>

<span data-ttu-id="895d9-112">Questo metodo aggiunge un campione alla parte finale della coda.</span><span class="sxs-lookup"><span data-stu-id="895d9-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="895d9-113">Mantenere la sezione critica prima di chiamare questo metodo e chiamarla solo quando l'oggetto utilizza un thread per recapitare esempi.</span><span class="sxs-lookup"><span data-stu-id="895d9-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="895d9-114">Per determinare se l'oggetto utilizza un thread, chiamare il metodo [**COutputQueue:: di Accodamento**](coutputqueue-isqueued.md) .</span><span class="sxs-lookup"><span data-stu-id="895d9-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="895d9-115">Questo metodo può essere utilizzato anche per inserire i messaggi di controllo nella coda.</span><span class="sxs-lookup"><span data-stu-id="895d9-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="895d9-116">Un messaggio di controllo è una costante definita (di cui viene eseguito il cast a un \_ tipo Long PTR) che indica al thread di eseguire un'azione.</span><span class="sxs-lookup"><span data-stu-id="895d9-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="895d9-117">La classe **COutputQueue** definisce i messaggi di controllo mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="895d9-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="895d9-118">Message</span><span class="sxs-lookup"><span data-stu-id="895d9-118">Message</span></span>       | <span data-ttu-id="895d9-119">Azione</span><span class="sxs-lookup"><span data-stu-id="895d9-119">Action</span></span>                                 |
| <span data-ttu-id="895d9-120">\_pacchetto EOS</span><span class="sxs-lookup"><span data-stu-id="895d9-120">EOS\_PACKET</span></span>   | <span data-ttu-id="895d9-121">Recapitare una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="895d9-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="895d9-122">NUOVO \_ segmento</span><span class="sxs-lookup"><span data-stu-id="895d9-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="895d9-123">Recapitare un nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="895d9-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="895d9-124">Reimposta \_ pacchetto</span><span class="sxs-lookup"><span data-stu-id="895d9-124">RESET\_PACKET</span></span> | <span data-ttu-id="895d9-125">Reimpostare lo stato della coda.</span><span class="sxs-lookup"><span data-stu-id="895d9-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="895d9-126">Invia \_ pacchetto</span><span class="sxs-lookup"><span data-stu-id="895d9-126">SEND\_PACKET</span></span>  | <span data-ttu-id="895d9-127">Inviare un batch parziale di campioni.</span><span class="sxs-lookup"><span data-stu-id="895d9-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="895d9-128">Si tratta di un metodo protetto, che la classe **COutputQueue** utilizza internamente.</span><span class="sxs-lookup"><span data-stu-id="895d9-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="895d9-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="895d9-129">Requirements</span></span>



| <span data-ttu-id="895d9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="895d9-130">Requirement</span></span> | <span data-ttu-id="895d9-131">Valore</span><span class="sxs-lookup"><span data-stu-id="895d9-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895d9-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="895d9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="895d9-133"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="895d9-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="895d9-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="895d9-134">Library</span></span><br/> | <dl> <span data-ttu-id="895d9-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="895d9-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="895d9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="895d9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="895d9-137">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="895d9-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




