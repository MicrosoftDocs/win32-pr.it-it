---
description: Usa la funzione SuspendThread di Microsoft Win32 per sospendere l'operazione di un thread in esecuzione.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Metodo CMsgThread. SuspendThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333312"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="bcb96-103">CMsgThread. SuspendThread, metodo</span><span class="sxs-lookup"><span data-stu-id="bcb96-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="bcb96-104">Usa la funzione **SuspendThread** di Microsoft Win32 per sospendere l'operazione di un thread in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bcb96-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb96-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcb96-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="bcb96-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcb96-106">Parameters</span></span>

<span data-ttu-id="bcb96-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bcb96-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcb96-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcb96-108">Return value</span></span>

<span data-ttu-id="bcb96-109">Se la funzione membro ha esito positivo, il valore restituito è il conteggio di sospensione precedente del thread.</span><span class="sxs-lookup"><span data-stu-id="bcb96-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="bcb96-110">Se la funzione membro ha esito negativo, il valore restituito è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="bcb96-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="bcb96-111">Per ottenere informazioni estese sull'errore, chiamare la funzione **GetLastError** di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="bcb96-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb96-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcb96-112">Remarks</span></span>

<span data-ttu-id="bcb96-113">Il thread client chiama questa funzione membro per sospendere l'operazione del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bcb96-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="bcb96-114">Il thread di lavoro rimane sospeso e non verrà eseguito fino a quando non viene effettuata una chiamata aggiuntiva alla funzione membro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb96-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb96-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcb96-115">Requirements</span></span>



| <span data-ttu-id="bcb96-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb96-116">Requirement</span></span> | <span data-ttu-id="bcb96-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb96-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb96-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcb96-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bcb96-119"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb96-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bcb96-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="bcb96-120">Library</span></span><br/> | <dl> <span data-ttu-id="bcb96-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb96-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb96-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcb96-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb96-123">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="bcb96-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




