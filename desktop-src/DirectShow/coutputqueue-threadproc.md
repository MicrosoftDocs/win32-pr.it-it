---
description: Il metodo ThreadProc recupera campioni dalla coda e li recapita al pin di input.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Metodo COutputQueue. ThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324669"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="0f94a-103">COutputQueue. ThreadProc, metodo</span><span class="sxs-lookup"><span data-stu-id="0f94a-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="0f94a-104">Il `ThreadProc` metodo recupera campioni dalla coda e li recapita al pin di input.</span><span class="sxs-lookup"><span data-stu-id="0f94a-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f94a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f94a-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="0f94a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f94a-106">Parameters</span></span>

<span data-ttu-id="0f94a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0f94a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f94a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f94a-108">Return value</span></span>

<span data-ttu-id="0f94a-109">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0f94a-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f94a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f94a-110">Remarks</span></span>

<span data-ttu-id="0f94a-111">Il metodo [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) chiama questo metodo, che implementa il ciclo del thread principale.</span><span class="sxs-lookup"><span data-stu-id="0f94a-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="0f94a-112">All'interno del ciclo, il metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f94a-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="0f94a-113">Recupera un esempio per la coda.</span><span class="sxs-lookup"><span data-stu-id="0f94a-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="0f94a-114">Se l'esempio è un messaggio di controllo, il thread esegue l'azione di controllo.</span><span class="sxs-lookup"><span data-stu-id="0f94a-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="0f94a-115">In caso contrario, inserisce l'esempio nella matrice [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .</span><span class="sxs-lookup"><span data-stu-id="0f94a-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="0f94a-116">Quando la matrice è completa (o se [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) è **false**), il thread chiama il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) per recapitare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="0f94a-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="0f94a-117">Se nessun campione viene accodato, il thread resta in attesa sul semaforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="0f94a-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="0f94a-118">Il thread termina quando la variabile membro [**COutputQueue:: m \_ BTerminate**](coutputqueue-m-bterminate.md) diventa **true**.</span><span class="sxs-lookup"><span data-stu-id="0f94a-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f94a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f94a-119">Requirements</span></span>



| <span data-ttu-id="0f94a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f94a-120">Requirement</span></span> | <span data-ttu-id="0f94a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0f94a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f94a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f94a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0f94a-123"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f94a-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f94a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f94a-124">Library</span></span><br/> | <dl> <span data-ttu-id="0f94a-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0f94a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f94a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f94a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f94a-127">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="0f94a-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




