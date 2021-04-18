---
description: Il metodo Advise Invia tutte le richieste pianificate per un periodo di tempo specificato o un valore precedente.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Metodo CAMSchedule. Advise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329571"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="03c84-103">Metodo CAMSchedule. Advise</span><span class="sxs-lookup"><span data-stu-id="03c84-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="03c84-104">Il `Advise` metodo invia tutte le richieste pianificate per un periodo di tempo specificato o un valore precedente.</span><span class="sxs-lookup"><span data-stu-id="03c84-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c84-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="03c84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c84-107">*rtTime* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="03c84-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="03c84-108">Valore che specifica l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="03c84-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c84-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03c84-109">Return value</span></span>

<span data-ttu-id="03c84-110">Restituisce l'ora di riferimento della richiesta di notifica pianificata successiva o il \_ tempo massimo se non ne è rimasto alcuno.</span><span class="sxs-lookup"><span data-stu-id="03c84-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="03c84-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c84-111">Remarks</span></span>

<span data-ttu-id="03c84-112">Quando il clock chiama questo metodo, specifica l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="03c84-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="03c84-113">L'utilità di pianificazione determina quali richieste di notifica sono scadute, se presenti, e le invia.</span><span class="sxs-lookup"><span data-stu-id="03c84-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="03c84-114">Se una richiesta di una volta scade, l'utilità di pianificazione la Elimina.</span><span class="sxs-lookup"><span data-stu-id="03c84-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="03c84-115">Se una richiesta periodica scade, l'utilità di pianificazione lo Ripianifica per il successivo tempo di notifica.</span><span class="sxs-lookup"><span data-stu-id="03c84-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="03c84-116">Il metodo restituisce l'ora della richiesta in sospeso successiva.</span><span class="sxs-lookup"><span data-stu-id="03c84-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="03c84-117">Per inviare una richiesta di notifica, l'utilità di pianificazione segnala l'evento o il semaforo specificato nel parametro *hNotify* del metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="03c84-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c84-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c84-118">Requirements</span></span>



| <span data-ttu-id="03c84-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c84-119">Requirement</span></span> | <span data-ttu-id="03c84-120">Valore</span><span class="sxs-lookup"><span data-stu-id="03c84-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c84-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03c84-121">Header</span></span><br/>  | <dl> <span data-ttu-id="03c84-122"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03c84-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="03c84-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="03c84-123">Library</span></span><br/> | <dl> <span data-ttu-id="03c84-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="03c84-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c84-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03c84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c84-126">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="03c84-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




