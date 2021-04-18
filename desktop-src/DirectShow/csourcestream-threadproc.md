---
description: 'Il metodo ThreadProc è la procedura del thread per il thread di lavoro. Questo metodo implementa il metodo CAMThread:: ThreadProc virtuale puro.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Metodo CSourceStream. ThreadProc (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325658"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="2185a-104">CSourceStream. ThreadProc, metodo</span><span class="sxs-lookup"><span data-stu-id="2185a-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="2185a-105">Il `ThreadProc` metodo è la procedura del thread per il thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2185a-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="2185a-106">Questo metodo implementa il metodo [**CAMThread:: ThreadProc**](camthread-threadproc.md) virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="2185a-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2185a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2185a-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="2185a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2185a-108">Parameters</span></span>

<span data-ttu-id="2185a-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2185a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2185a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2185a-110">Return value</span></span>

<span data-ttu-id="2185a-111">Restituisce 0 se il thread è stato completato correttamente o 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2185a-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="2185a-112">Se il valore restituito è 1, le risorse del thread potrebbero ancora essere allocate.</span><span class="sxs-lookup"><span data-stu-id="2185a-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="2185a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2185a-113">Remarks</span></span>

<span data-ttu-id="2185a-114">Questo metodo attende a tempo indefinito per le richieste di thread, chiamando il metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="2185a-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="2185a-115">Se riceve una richiesta [**CSourceStream:: Run**](csourcestream-run.md) o [**CSourceStream::P ause**](csourcestream-pause.md) , chiama il metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="2185a-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="2185a-116">Il metodo **DoBufferProcessingLoop** esegue il push dei dati fino a quando non riceve una richiesta [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="2185a-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="2185a-117">La procedura del thread viene chiusa quando riceve una richiesta [**CSourceStream:: Exit**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="2185a-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="2185a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2185a-118">Requirements</span></span>



| <span data-ttu-id="2185a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2185a-119">Requirement</span></span> | <span data-ttu-id="2185a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2185a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2185a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2185a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2185a-122"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2185a-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2185a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="2185a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2185a-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2185a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2185a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2185a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2185a-126">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="2185a-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




