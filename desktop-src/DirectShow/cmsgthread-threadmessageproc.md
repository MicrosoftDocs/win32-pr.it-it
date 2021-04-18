---
description: Elabora le richieste. Si tratta di una funzione membro virtuale pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Metodo CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330222"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="93d44-104">CMsgThread. ThreadMessageProc, metodo</span><span class="sxs-lookup"><span data-stu-id="93d44-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="93d44-105">Elabora le richieste.</span><span class="sxs-lookup"><span data-stu-id="93d44-105">Processes requests.</span></span> <span data-ttu-id="93d44-106">Si tratta di una funzione membro virtuale pura.</span><span class="sxs-lookup"><span data-stu-id="93d44-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93d44-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="93d44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93d44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d44-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="93d44-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="93d44-110">Codice della richiesta.</span><span class="sxs-lookup"><span data-stu-id="93d44-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="93d44-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="93d44-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="93d44-112">Parametro facoltativo del flag da richiedere.</span><span class="sxs-lookup"><span data-stu-id="93d44-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="93d44-113">*lpParam*</span><span class="sxs-lookup"><span data-stu-id="93d44-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93d44-114">Puntatore facoltativo a dati aggiuntivi o a un blocco di dati restituito.</span><span class="sxs-lookup"><span data-stu-id="93d44-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="93d44-115">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="93d44-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="93d44-116">Puntatore facoltativo a un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="93d44-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d44-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93d44-117">Return value</span></span>

<span data-ttu-id="93d44-118">Qualsiasi valore restituito diverso da zero causa la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="93d44-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="93d44-119">Restituisce zero a meno che non sia stata elaborata di recente una richiesta di uscita.</span><span class="sxs-lookup"><span data-stu-id="93d44-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d44-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="93d44-120">Remarks</span></span>

<span data-ttu-id="93d44-121">Questa funzione virtuale pura deve essere sottoposta a override nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="93d44-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="93d44-122">Verrà chiamata una volta per ogni richiesta accodata da una chiamata alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="93d44-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="93d44-123">La funzione membro definisce i quattro parametri.</span><span class="sxs-lookup"><span data-stu-id="93d44-123">The member function defines the four parameters.</span></span> <span data-ttu-id="93d44-124">In genere, usare il parametro *uMsg* per indicare la richiesta e gli altri tre parametri saranno parametri aggiuntivi facoltativi.</span><span class="sxs-lookup"><span data-stu-id="93d44-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="93d44-125">Se l'applicazione lo richiede, l'applicazione chiamante può fornire un puntatore a un oggetto [**CAMEvent**](camevent.md) nel parametro *pEvent* .</span><span class="sxs-lookup"><span data-stu-id="93d44-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="93d44-126">È necessario impostare questo evento dopo l'elaborazione dell'evento usando un'espressione simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="93d44-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="93d44-127">È necessario riservare un codice di richiesta per indicare al thread di lavoro di uscire.</span><span class="sxs-lookup"><span data-stu-id="93d44-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="93d44-128">Al momento della ricezione della richiesta, restituire 1 da questa funzione membro.</span><span class="sxs-lookup"><span data-stu-id="93d44-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="93d44-129">Restituisce 0 se non si desidera che il thread di lavoro venga chiuso.</span><span class="sxs-lookup"><span data-stu-id="93d44-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d44-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93d44-130">Requirements</span></span>



| <span data-ttu-id="93d44-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d44-131">Requirement</span></span> | <span data-ttu-id="93d44-132">Valore</span><span class="sxs-lookup"><span data-stu-id="93d44-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d44-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93d44-133">Header</span></span><br/>  | <dl> <span data-ttu-id="93d44-134"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93d44-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="93d44-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="93d44-135">Library</span></span><br/> | <dl> <span data-ttu-id="93d44-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="93d44-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d44-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93d44-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d44-138">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="93d44-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




