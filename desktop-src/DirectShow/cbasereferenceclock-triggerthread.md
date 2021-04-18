---
description: Il metodo TriggerThread attiva il thread di lavoro che gestisce la pianificazione.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Metodo CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332219"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="99406-103">CBaseReferenceClock. TriggerThread, metodo</span><span class="sxs-lookup"><span data-stu-id="99406-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="99406-104">Il `TriggerThread` metodo attiva il thread di lavoro che gestisce la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="99406-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="99406-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99406-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="99406-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99406-106">Parameters</span></span>

<span data-ttu-id="99406-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="99406-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99406-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99406-108">Return value</span></span>

<span data-ttu-id="99406-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="99406-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99406-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="99406-110">Remarks</span></span>

<span data-ttu-id="99406-111">Il clock usa un thread di lavoro che chiama il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) in momenti appropriati.</span><span class="sxs-lookup"><span data-stu-id="99406-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="99406-112">La classe derivata può chiamare `TriggerThread` per riattivare il thread.</span><span class="sxs-lookup"><span data-stu-id="99406-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="99406-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99406-113">Requirements</span></span>



| <span data-ttu-id="99406-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99406-114">Requirement</span></span> | <span data-ttu-id="99406-115">Valore</span><span class="sxs-lookup"><span data-stu-id="99406-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99406-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99406-116">Header</span></span><br/>  | <dl> <span data-ttu-id="99406-117"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99406-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99406-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="99406-118">Library</span></span><br/> | <dl> <span data-ttu-id="99406-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99406-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99406-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99406-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99406-121">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="99406-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




