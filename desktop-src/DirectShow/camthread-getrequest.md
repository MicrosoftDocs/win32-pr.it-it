---
description: Il metodo GetRequest attende la richiesta successiva.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Metodo CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329878"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="56ee8-103">Metodo CAMThread. GetRequest</span><span class="sxs-lookup"><span data-stu-id="56ee8-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="56ee8-104">Il `GetRequest` metodo attende la richiesta successiva.</span><span class="sxs-lookup"><span data-stu-id="56ee8-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ee8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56ee8-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="56ee8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56ee8-106">Parameters</span></span>

<span data-ttu-id="56ee8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="56ee8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56ee8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56ee8-108">Return value</span></span>

<span data-ttu-id="56ee8-109">Restituisce un valore definito dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="56ee8-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ee8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="56ee8-110">Remarks</span></span>

<span data-ttu-id="56ee8-111">Questo metodo si blocca fino a quando un altro thread chiama il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="56ee8-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="56ee8-112">Restituisce quindi il parametro passato a CallWorker.</span><span class="sxs-lookup"><span data-stu-id="56ee8-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="56ee8-113">Chiamare il metodo [**CAMThread:: Reply**](camthread-reply.md) per rilasciare il thread richiedente.</span><span class="sxs-lookup"><span data-stu-id="56ee8-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ee8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56ee8-114">Requirements</span></span>



| <span data-ttu-id="56ee8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ee8-115">Requirement</span></span> | <span data-ttu-id="56ee8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="56ee8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ee8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56ee8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56ee8-118"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56ee8-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="56ee8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="56ee8-119">Library</span></span><br/> | <dl> <span data-ttu-id="56ee8-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56ee8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ee8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56ee8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ee8-122">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="56ee8-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




