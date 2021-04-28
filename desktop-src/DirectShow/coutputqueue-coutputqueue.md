---
description: 'Costruttore COutputQueue.COutputQueue : metodo del costruttore.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Costruttore COutputQueue.COutputQueue (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095329"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="cda8f-103">Costruttore COutputQueue.COutputQueue</span><span class="sxs-lookup"><span data-stu-id="cda8f-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="cda8f-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="cda8f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cda8f-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="cda8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cda8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda8f-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="cda8f-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-108">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input.</span><span class="sxs-lookup"><span data-stu-id="cda8f-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="cda8f-109">L'oggetto consegnerà esempi a questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="cda8f-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cda8f-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-111">Puntatore a un **codice restituito HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="cda8f-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="cda8f-112">Impostare il valore su S \_ OK prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cda8f-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="cda8f-113">In caso di restituzione, *phr* riceve un valore che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="cda8f-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="cda8f-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-115">Flag che specifica se l'oggetto decide quando creare una coda.</span><span class="sxs-lookup"><span data-stu-id="cda8f-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="cda8f-116">Se **TRUE,** l'oggetto crea una coda solo se il pin di input potrebbe bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="cda8f-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="cda8f-117">Se **FALSE,** il *parametro bQueue* specifica se creare una coda.</span><span class="sxs-lookup"><span data-stu-id="cda8f-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="cda8f-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-119">Se *bAuto* è **TRUE,** questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="cda8f-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="cda8f-120">Se *bAuto* è **FALSE,** questo flag specifica se creare una coda.</span><span class="sxs-lookup"><span data-stu-id="cda8f-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="cda8f-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-122">Numero massimo di campioni da distribuire in un batch.</span><span class="sxs-lookup"><span data-stu-id="cda8f-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="cda8f-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-124">Flag che specifica se usare dimensioni esatte dei batch.</span><span class="sxs-lookup"><span data-stu-id="cda8f-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="cda8f-125">Se **TRUE,** l'oggetto attende gli *esempi lBatchSize* prima di recapitarli al pin di input.</span><span class="sxs-lookup"><span data-stu-id="cda8f-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="cda8f-126">Se **FALSE,** l'oggetto recapita gli esempi quando li riceve.</span><span class="sxs-lookup"><span data-stu-id="cda8f-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="cda8f-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-128">Dimensioni della cache per la coda.</span><span class="sxs-lookup"><span data-stu-id="cda8f-128">Cache size for the queue.</span></span> <span data-ttu-id="cda8f-129">Il valore predefinito, DEFAULTCACHE, è una costante definita per la [**classe CBaseList.**](cbaselist.md)</span><span class="sxs-lookup"><span data-stu-id="cda8f-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="cda8f-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="cda8f-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="cda8f-131">Priorità del thread che recapita gli esempi.</span><span class="sxs-lookup"><span data-stu-id="cda8f-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cda8f-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="cda8f-132">Remarks</span></span>

<span data-ttu-id="cda8f-133">Se *bAuto* è **TRUE,** l'oggetto chiama il metodo [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sul pin downstream.</span><span class="sxs-lookup"><span data-stu-id="cda8f-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="cda8f-134">Se **ReceiveCanBlock restituisce** S OK (ovvero il pin potrebbe bloccarsi nelle chiamate \_ [**IMemInputPin::Receive),**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) l'oggetto crea un thread per la distribuzione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="cda8f-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="cda8f-135">In caso contrario, non crea un thread.</span><span class="sxs-lookup"><span data-stu-id="cda8f-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="cda8f-136">Se *bAuto* è **FALSE,** il valore di *bQueue* determina se creare un thread.</span><span class="sxs-lookup"><span data-stu-id="cda8f-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="cda8f-137">Se l'oggetto crea un thread, assegna l'handle del thread alla variabile membro [**COutputQueue::m \_ hThread.**](coutputqueue-m-hthread.md)</span><span class="sxs-lookup"><span data-stu-id="cda8f-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="cda8f-138">La routine del thread [**è COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md)e il parametro thread è un puntatore a questo.</span><span class="sxs-lookup"><span data-stu-id="cda8f-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="cda8f-139">L'oggetto crea anche una coda per contenere gli esempi, specificata dalla variabile membro [**COutputQueue::m \_ List.**](coutputqueue-m-list.md)</span><span class="sxs-lookup"><span data-stu-id="cda8f-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda8f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cda8f-140">Requirements</span></span>



| <span data-ttu-id="cda8f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda8f-141">Requirement</span></span> | <span data-ttu-id="cda8f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="cda8f-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda8f-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cda8f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="cda8f-144"><dt>Outputq.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cda8f-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cda8f-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="cda8f-145">Library</span></span><br/> | <dl> <span data-ttu-id="cda8f-146"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cda8f-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda8f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cda8f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda8f-148">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="cda8f-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




