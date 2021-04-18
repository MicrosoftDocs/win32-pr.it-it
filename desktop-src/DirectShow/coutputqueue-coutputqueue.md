---
description: Metodo del costruttore.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Costruttore COutputQueue. COutputQueue (Outputq. h)
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
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330212"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="0ea00-103">Costruttore COutputQueue. COutputQueue</span><span class="sxs-lookup"><span data-stu-id="0ea00-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="0ea00-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0ea00-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ea00-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ea00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ea00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea00-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="0ea00-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="0ea00-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="0ea00-109">L'oggetto fornirà esempi a questo pin.</span><span class="sxs-lookup"><span data-stu-id="0ea00-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-110">*PHR*</span><span class="sxs-lookup"><span data-stu-id="0ea00-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-111">Puntatore a un codice restituito **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ea00-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="0ea00-112">Impostare il valore su S \_ OK prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0ea00-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="0ea00-113">Al ritorno, *PHR* riceve un valore che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="0ea00-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="0ea00-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-115">Flag che specifica se l'oggetto decide quando creare una coda.</span><span class="sxs-lookup"><span data-stu-id="0ea00-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="0ea00-116">Se **true**, l'oggetto crea una coda solo se il pin di input potrebbe bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="0ea00-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="0ea00-117">Se **false**, il parametro *bQueue* specifica se creare una coda.</span><span class="sxs-lookup"><span data-stu-id="0ea00-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="0ea00-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-119">Se *bAuto* è **true**, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0ea00-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="0ea00-120">Se *bAuto* è **false**, questo flag specifica se creare una coda.</span><span class="sxs-lookup"><span data-stu-id="0ea00-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="0ea00-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-122">Numero massimo di campioni da recapitare in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="0ea00-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="0ea00-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-124">Flag che specifica se utilizzare le dimensioni esatte dei batch.</span><span class="sxs-lookup"><span data-stu-id="0ea00-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="0ea00-125">Se **true**, l'oggetto attende gli esempi di *lBatchSize* prima di distribuirli al pin di input.</span><span class="sxs-lookup"><span data-stu-id="0ea00-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="0ea00-126">Se **false**, l'oggetto recapita gli esempi mentre li riceve.</span><span class="sxs-lookup"><span data-stu-id="0ea00-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="0ea00-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-128">Dimensioni della cache per la coda.</span><span class="sxs-lookup"><span data-stu-id="0ea00-128">Cache size for the queue.</span></span> <span data-ttu-id="0ea00-129">Il valore predefinito, DEFAULTCACHE, è una costante definita per la classe [**CBaseList**](cbaselist.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea00-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ea00-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="0ea00-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea00-131">Priorità del thread che fornisce esempi.</span><span class="sxs-lookup"><span data-stu-id="0ea00-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ea00-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ea00-132">Remarks</span></span>

<span data-ttu-id="0ea00-133">Se *bAuto* è **true**, l'oggetto chiama il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sul pin downstream.</span><span class="sxs-lookup"><span data-stu-id="0ea00-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="0ea00-134">Se **ReceiveCanBlock** restituisce \_ OK (ovvero il PIN potrebbe bloccarsi in [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Calls), l'oggetto crea un thread per la distribuzione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="0ea00-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="0ea00-135">In caso contrario, non crea un thread.</span><span class="sxs-lookup"><span data-stu-id="0ea00-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="0ea00-136">Se *bAuto* è **false**, il valore di *bQueue* determina se creare un thread.</span><span class="sxs-lookup"><span data-stu-id="0ea00-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="0ea00-137">Se l'oggetto crea un thread, assegna l'handle del thread alla variabile membro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea00-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="0ea00-138">La routine thread è [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)e il parametro thread è un puntatore a questo.</span><span class="sxs-lookup"><span data-stu-id="0ea00-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="0ea00-139">L'oggetto crea anche una coda per contenere gli esempi, fornita dalla variabile membro dell' [**\_ elenco COutputQueue:: m**](coutputqueue-m-list.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea00-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea00-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ea00-140">Requirements</span></span>



| <span data-ttu-id="0ea00-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea00-141">Requirement</span></span> | <span data-ttu-id="0ea00-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0ea00-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea00-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ea00-143">Header</span></span><br/>  | <dl> <span data-ttu-id="0ea00-144"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea00-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ea00-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ea00-145">Library</span></span><br/> | <dl> <span data-ttu-id="0ea00-146"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea00-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea00-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ea00-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea00-148">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="0ea00-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




