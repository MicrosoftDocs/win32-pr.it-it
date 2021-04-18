---
description: Il metodo AddAdvisePacket aggiunge una richiesta di notifica all'elenco di richieste in sospeso.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Metodo CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329572"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="e0187-103">CAMSchedule. AddAdvisePacket, metodo</span><span class="sxs-lookup"><span data-stu-id="e0187-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="e0187-104">Il `AddAdvisePacket` metodo aggiunge una richiesta di notifica all'elenco di richieste in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e0187-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0187-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0187-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="e0187-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0187-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0187-107">*time1* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="e0187-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e0187-108">Tempo richiesto per l'avviso.</span><span class="sxs-lookup"><span data-stu-id="e0187-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="e0187-109">*time2* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="e0187-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e0187-110">Per richieste di notifica periodiche, tempo tra le notifiche.</span><span class="sxs-lookup"><span data-stu-id="e0187-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="e0187-111">Questo parametro viene ignorato se *bPeriodic* è **false**.</span><span class="sxs-lookup"><span data-stu-id="e0187-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0187-112">*hNotify*</span><span class="sxs-lookup"><span data-stu-id="e0187-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="e0187-113">Handle per un semaforo se *bPeriodic* è **true** oppure handle a un evento se *bPeriodic* è **false**.</span><span class="sxs-lookup"><span data-stu-id="e0187-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0187-114">*bPeriodic*</span><span class="sxs-lookup"><span data-stu-id="e0187-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="e0187-115">Valore booleano che specifica se aggiungere una notifica periodica o una notifica monouso.</span><span class="sxs-lookup"><span data-stu-id="e0187-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="e0187-116">Se **true**, la notifica è periodica; il parametro *time2* specifica l'intervallo tra le notifiche.</span><span class="sxs-lookup"><span data-stu-id="e0187-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="e0187-117">Se **false**, la notifica viene eseguita una sola volta.</span><span class="sxs-lookup"><span data-stu-id="e0187-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0187-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0187-118">Return value</span></span>

<span data-ttu-id="e0187-119">Restituisce un identificatore per la richiesta di notifica (il "cookie").</span><span class="sxs-lookup"><span data-stu-id="e0187-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="e0187-120">Se il metodo ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="e0187-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0187-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0187-121">Requirements</span></span>



| <span data-ttu-id="e0187-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0187-122">Requirement</span></span> | <span data-ttu-id="e0187-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e0187-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0187-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0187-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e0187-125"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0187-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="e0187-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0187-126">Library</span></span><br/> | <dl> <span data-ttu-id="e0187-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e0187-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0187-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0187-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0187-129">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="e0187-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




