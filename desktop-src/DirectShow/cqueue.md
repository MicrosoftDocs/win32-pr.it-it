---
description: Il modello di classe CQueue implementa una coda semplice e a dimensione statica.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Classe CQueue (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331322"
---
# <a name="cqueue-class"></a><span data-ttu-id="1ec6f-103">Classe CQueue</span><span class="sxs-lookup"><span data-stu-id="1ec6f-103">CQueue class</span></span>

<span data-ttu-id="1ec6f-104">Il modello di classe **CQueue** implementa una coda semplice e a dimensione statica.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="1ec6f-105">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="1ec6f-105">Public Methods</span></span>                                  | <span data-ttu-id="1ec6f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ec6f-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="1ec6f-107">**CQueue**</span><span class="sxs-lookup"><span data-stu-id="1ec6f-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="1ec6f-108">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="1ec6f-109">**~ CQueue**</span><span class="sxs-lookup"><span data-stu-id="1ec6f-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="1ec6f-110">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="1ec6f-111">**GetQueueObject**</span><span class="sxs-lookup"><span data-stu-id="1ec6f-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="1ec6f-112">Recupera l'elemento successivo dalla coda.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="1ec6f-113">**PutQueueObject**</span><span class="sxs-lookup"><span data-stu-id="1ec6f-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="1ec6f-114">Inserisce un elemento nella coda.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="1ec6f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ec6f-115">Remarks</span></span>

<span data-ttu-id="1ec6f-116">Il costruttore della classe specifica le dimensioni della coda.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="1ec6f-117">Usare [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) per inserire un elemento nella coda e il metodo [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) per rimuovere dalla coda un elemento.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="1ec6f-118">Se la coda è piena, il metodo **PutQueueObject** si blocca fino a quando un elemento non viene rimosso dalla coda.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="1ec6f-119">Se la coda è vuota, il **GetQueueObject** si blocca fino a quando un elemento non viene accodato.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="1ec6f-120">Il parametro di modello specifica il tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="1ec6f-121">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1ec6f-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="1ec6f-122">La classe usa due semafori per controllare le operazioni di Accodamento, un semaforo "Get" e un semaforo "put".</span><span class="sxs-lookup"><span data-stu-id="1ec6f-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="1ec6f-123">Il metodo [**GetQueueObject**](cqueue-getqueueobject.md) attende il semaforo "Get" (usando la funzione **WaitForSingleObject** ) e rilascia il semaforo "put" (usando la funzione **ReleaseSemaphore** ).</span><span class="sxs-lookup"><span data-stu-id="1ec6f-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="1ec6f-124">Il metodo [**PutQueueObject**](cqueue-putqueueobject.md) attende il semaforo "put" e rilascia il semaforo "Get".</span><span class="sxs-lookup"><span data-stu-id="1ec6f-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="1ec6f-125">La classe utilizza una sezione critica per serializzare le operazioni di Accodamento tra più thread.</span><span class="sxs-lookup"><span data-stu-id="1ec6f-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec6f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ec6f-126">Requirements</span></span>



| <span data-ttu-id="1ec6f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec6f-127">Requirement</span></span> | <span data-ttu-id="1ec6f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1ec6f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec6f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ec6f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec6f-130"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec6f-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1ec6f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ec6f-131">Library</span></span><br/> | <dl> <span data-ttu-id="1ec6f-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec6f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




