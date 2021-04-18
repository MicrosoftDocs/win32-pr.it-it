---
description: "Il metodo GetRequestHandle recupera un handle per l'evento segnalato dal metodo CAMThread:: CallWorker."
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Metodo CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330860"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="b82cf-103">CAMThread. GetRequestHandle, metodo</span><span class="sxs-lookup"><span data-stu-id="b82cf-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="b82cf-104">Il `GetRequestHandle` metodo recupera un handle per l'evento segnalato dal metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="b82cf-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b82cf-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="b82cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b82cf-106">Parameters</span></span>

<span data-ttu-id="b82cf-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b82cf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b82cf-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b82cf-108">Return value</span></span>

<span data-ttu-id="b82cf-109">Restituisce un handle di evento.</span><span class="sxs-lookup"><span data-stu-id="b82cf-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="b82cf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b82cf-110">Remarks</span></span>

<span data-ttu-id="b82cf-111">La classe CAMEvent mantiene un evento di reimpostazione manuale privato, che viene impostato da CallWorker e reimpostato dal metodo [**CAMThread:: Reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="b82cf-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="b82cf-112">Se si chiama una funzione come WaitForMultipleObjects, utilizzare GetRequestHandle per recuperare l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b82cf-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82cf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b82cf-113">Requirements</span></span>



| <span data-ttu-id="b82cf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b82cf-114">Requirement</span></span> | <span data-ttu-id="b82cf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b82cf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b82cf-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b82cf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b82cf-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b82cf-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b82cf-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b82cf-118">Library</span></span><br/> | <dl> <span data-ttu-id="b82cf-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b82cf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b82cf-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b82cf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82cf-121">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="b82cf-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




