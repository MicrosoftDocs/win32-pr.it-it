---
description: Il metodo CallWorker segnala al thread la richiesta.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Metodo CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331461"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="1912d-103">CAMThread. CallWorker, metodo</span><span class="sxs-lookup"><span data-stu-id="1912d-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="1912d-104">Il `CallWorker` metodo segnala al thread la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1912d-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1912d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1912d-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="1912d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1912d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1912d-107">*dwParam*</span><span class="sxs-lookup"><span data-stu-id="1912d-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1912d-108">Parametro della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1912d-108">Request parameter.</span></span> <span data-ttu-id="1912d-109">La classe derivata definisce il significato del parametro.</span><span class="sxs-lookup"><span data-stu-id="1912d-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1912d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1912d-110">Return value</span></span>

<span data-ttu-id="1912d-111">Restituisce un valore definito dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="1912d-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="1912d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1912d-112">Remarks</span></span>

<span data-ttu-id="1912d-113">I metodi [**CAMThread:: GetRequest**](camthread-getrequest.md) e [**CAMThread:: CheckRequest**](camthread-checkrequest.md) recuperano il valore del parametro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="1912d-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="1912d-114">Il metodo GetRequest si blocca fino a quando non `CallWorker` viene chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="1912d-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="1912d-115">Questo metodo si blocca fino a quando non viene chiamato il metodo [**CAMThread:: Reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="1912d-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="1912d-116">Il valore restituito è il parametro assegnato a Reply.</span><span class="sxs-lookup"><span data-stu-id="1912d-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="1912d-117">Questo metodo include il blocco [**CAMThread:: m \_ AccessLock**](camthread-m-accesslock.md) per serializzare le richieste.</span><span class="sxs-lookup"><span data-stu-id="1912d-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="1912d-118">Pertanto, chiamare questo metodo dal thread stesso o da qualsiasi funzione membro eseguita nel contesto del thread.</span><span class="sxs-lookup"><span data-stu-id="1912d-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="1912d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1912d-119">Requirements</span></span>



| <span data-ttu-id="1912d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1912d-120">Requirement</span></span> | <span data-ttu-id="1912d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1912d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1912d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1912d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1912d-123"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1912d-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1912d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1912d-124">Library</span></span><br/> | <dl> <span data-ttu-id="1912d-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1912d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1912d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1912d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1912d-127">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="1912d-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




