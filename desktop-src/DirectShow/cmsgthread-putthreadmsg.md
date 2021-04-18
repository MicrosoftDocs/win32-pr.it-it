---
description: Accoda una richiesta di esecuzione da parte del thread di lavoro.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Metodo CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331290"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="89543-103">CMsgThread. PutThreadMsg, metodo</span><span class="sxs-lookup"><span data-stu-id="89543-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="89543-104">Accoda una richiesta di esecuzione da parte del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="89543-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="89543-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89543-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="89543-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89543-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89543-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="89543-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="89543-108">Codice della richiesta.</span><span class="sxs-lookup"><span data-stu-id="89543-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="89543-109">*dwMsgFlags*</span><span class="sxs-lookup"><span data-stu-id="89543-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="89543-110">Parametro flags facoltativo.</span><span class="sxs-lookup"><span data-stu-id="89543-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89543-111">*lpMsgParam*</span><span class="sxs-lookup"><span data-stu-id="89543-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89543-112">Puntatore facoltativo a un blocco di dati contenente parametri o valori restituiti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="89543-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="89543-113">Deve essere allocato in modo statico o heap e non automatico.</span><span class="sxs-lookup"><span data-stu-id="89543-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="89543-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="89543-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="89543-115">Puntatore facoltativo a un oggetto evento da segnalare al completamento.</span><span class="sxs-lookup"><span data-stu-id="89543-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89543-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89543-116">Return value</span></span>

<span data-ttu-id="89543-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="89543-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89543-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="89543-118">Remarks</span></span>

<span data-ttu-id="89543-119">Questa funzione membro accoda una richiesta di esecuzione da parte del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="89543-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="89543-120">I parametri di questa funzione membro verranno accodati (in un oggetto [**CMsg**](cmsg.md) ) e passati alla funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="89543-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="89543-121">Questa funzione membro viene restituita immediatamente dopo l'accodamento della richiesta e non attende che il thread soddisfi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="89543-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="89543-122">La funzione membro **CMsgThread:: ThreadMessageProc** della classe derivata definisce i quattro parametri.</span><span class="sxs-lookup"><span data-stu-id="89543-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="89543-123">Questa funzione membro usa un elenco multithread safe, quindi è possibile rendere sicure più chiamate a questa funzione membro da thread diversi.</span><span class="sxs-lookup"><span data-stu-id="89543-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="89543-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89543-124">Requirements</span></span>



| <span data-ttu-id="89543-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="89543-125">Requirement</span></span> | <span data-ttu-id="89543-126">Valore</span><span class="sxs-lookup"><span data-stu-id="89543-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89543-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89543-127">Header</span></span><br/>  | <dl> <span data-ttu-id="89543-128"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89543-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89543-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="89543-129">Library</span></span><br/> | <dl> <span data-ttu-id="89543-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89543-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89543-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89543-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89543-132">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="89543-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




