---
description: 'Il metodo AdvisePeriodic crea una richiesta di notifica periodica. Questo metodo implementa il metodo IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Metodo CBaseReferenceClock. AdvisePeriodic (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330305"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="88233-104">CBaseReferenceClock. AdvisePeriodic, metodo</span><span class="sxs-lookup"><span data-stu-id="88233-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="88233-105">Il `AdvisePeriodic` metodo crea una richiesta di notifica periodica.</span><span class="sxs-lookup"><span data-stu-id="88233-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="88233-106">Questo metodo implementa il metodo [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .</span><span class="sxs-lookup"><span data-stu-id="88233-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88233-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88233-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="88233-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88233-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88233-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="88233-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="88233-110">Ora della prima notifica, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="88233-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="88233-111">Deve essere maggiore di zero e minore del \_ tempo massimo.</span><span class="sxs-lookup"><span data-stu-id="88233-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="88233-112">*PeriodTime*</span><span class="sxs-lookup"><span data-stu-id="88233-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="88233-113">Tempo tra le notifiche, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="88233-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="88233-114">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="88233-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="88233-115">*hSemaphore*</span><span class="sxs-lookup"><span data-stu-id="88233-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="88233-116">Handle per un semaforo, creato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="88233-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="88233-117">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="88233-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="88233-118">Puntatore a una variabile che riceve un identificatore per la richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="88233-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88233-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88233-119">Return value</span></span>

<span data-ttu-id="88233-120">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="88233-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="88233-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="88233-121">Return code</span></span>                                                                                   | <span data-ttu-id="88233-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88233-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="88233-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88233-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="88233-124">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="88233-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="88233-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="88233-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="88233-126">Valori di ora non validi</span><span class="sxs-lookup"><span data-stu-id="88233-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="88233-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="88233-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="88233-128">Errore</span><span class="sxs-lookup"><span data-stu-id="88233-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="88233-129"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="88233-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="88233-130">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="88233-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88233-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="88233-131">Remarks</span></span>

<span data-ttu-id="88233-132">A ogni ora di notifica, il clock rilascia il semaforo specificato nel parametro *hSemaphore* .</span><span class="sxs-lookup"><span data-stu-id="88233-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="88233-133">Quando non sono necessarie altre notifiche, chiamare il metodo [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="88233-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="88233-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88233-134">Requirements</span></span>



| <span data-ttu-id="88233-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="88233-135">Requirement</span></span> | <span data-ttu-id="88233-136">Valore</span><span class="sxs-lookup"><span data-stu-id="88233-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88233-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88233-137">Header</span></span><br/>  | <dl> <span data-ttu-id="88233-138"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88233-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88233-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="88233-139">Library</span></span><br/> | <dl> <span data-ttu-id="88233-140"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88233-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88233-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88233-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88233-142">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="88233-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




