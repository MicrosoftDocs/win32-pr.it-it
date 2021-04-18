---
description: Il metodo Close attende la chiusura del thread, quindi rilascia le relative risorse.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Metodo CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331291"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="5f0df-103">Metodo CAMThread. Close</span><span class="sxs-lookup"><span data-stu-id="5f0df-103">CAMThread.Close method</span></span>

<span data-ttu-id="5f0df-104">Il `Close` metodo attende la chiusura del thread, quindi rilascia le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="5f0df-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f0df-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="5f0df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f0df-106">Parameters</span></span>

<span data-ttu-id="5f0df-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5f0df-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f0df-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f0df-108">Return value</span></span>

<span data-ttu-id="5f0df-109">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5f0df-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f0df-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f0df-110">Remarks</span></span>

<span data-ttu-id="5f0df-111">Prima di chiamare questo metodo, è necessario fornire un modo per uscire dal thread.</span><span class="sxs-lookup"><span data-stu-id="5f0df-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="5f0df-112">Nel metodo [**CAMThread:: ThreadProc**](camthread-threadproc.md) , ad esempio, definire una richiesta che segnali la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="5f0df-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="5f0df-113">Chiamare quindi il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) con tale valore.</span><span class="sxs-lookup"><span data-stu-id="5f0df-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="5f0df-114">Il metodo del distruttore [**~ CAMThread**](camthread--camthread.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5f0df-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0df-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f0df-115">Requirements</span></span>



| <span data-ttu-id="5f0df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0df-116">Requirement</span></span> | <span data-ttu-id="5f0df-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0df-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0df-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f0df-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5f0df-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0df-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5f0df-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f0df-120">Library</span></span><br/> | <dl> <span data-ttu-id="5f0df-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0df-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0df-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f0df-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0df-123">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="5f0df-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




