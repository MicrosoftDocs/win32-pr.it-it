---
description: 'Il metodo AdviseTime crea una richiesta di notifica di un solo tentativo. Questo metodo implementa il metodo IReferenceClock:: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Metodo CBaseReferenceClock. AdviseTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330307"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="d7c82-104">CBaseReferenceClock. AdviseTime, metodo</span><span class="sxs-lookup"><span data-stu-id="d7c82-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="d7c82-105">Il `AdviseTime` metodo crea una richiesta di notifica di un solo tentativo.</span><span class="sxs-lookup"><span data-stu-id="d7c82-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="d7c82-106">Questo metodo implementa il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .</span><span class="sxs-lookup"><span data-stu-id="d7c82-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c82-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7c82-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="d7c82-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7c82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c82-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="d7c82-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c82-110">Tempo di riferimento di base, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="d7c82-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="d7c82-111">*streamTime*</span><span class="sxs-lookup"><span data-stu-id="d7c82-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c82-112">Tempo di offset del flusso, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="d7c82-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="d7c82-113">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="d7c82-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c82-114">Handle per un evento, creato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="d7c82-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="d7c82-115">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="d7c82-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c82-116">Puntatore a una variabile che riceve un identificatore per la richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="d7c82-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c82-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7c82-117">Return value</span></span>

<span data-ttu-id="d7c82-118">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d7c82-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d7c82-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d7c82-119">Return code</span></span>                                                                                   | <span data-ttu-id="d7c82-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7c82-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d7c82-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d7c82-122">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="d7c82-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="d7c82-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d7c82-124">Valori di ora non validi</span><span class="sxs-lookup"><span data-stu-id="d7c82-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="d7c82-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d7c82-126">Errore</span><span class="sxs-lookup"><span data-stu-id="d7c82-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="d7c82-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d7c82-128">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="d7c82-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7c82-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7c82-129">Remarks</span></span>

<span data-ttu-id="d7c82-130">Questo metodo crea una richiesta di notifica monouso per l'ora di riferimento *baseTime*  +  *streamTime*.</span><span class="sxs-lookup"><span data-stu-id="d7c82-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="d7c82-131">La somma deve essere maggiore di zero e minore del \_ tempo massimo oppure il metodo restituisce e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d7c82-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="d7c82-132">Al momento richiesto, l'orologio segnala l'evento specificato nel parametro *hEvent* .</span><span class="sxs-lookup"><span data-stu-id="d7c82-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="d7c82-133">Per annullare la notifica prima del raggiungimento dell'ora, chiamare il metodo [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="d7c82-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="d7c82-134">Dopo che si è verificata la notifica, il clock lo cancella automaticamente, pertanto non è necessario chiamare **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="d7c82-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="d7c82-135">Tuttavia, non si tratta di un errore a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="d7c82-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c82-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7c82-136">Requirements</span></span>



| <span data-ttu-id="d7c82-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c82-137">Requirement</span></span> | <span data-ttu-id="d7c82-138">Valore</span><span class="sxs-lookup"><span data-stu-id="d7c82-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c82-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7c82-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c82-140"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7c82-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7c82-141">Library</span></span><br/> | <dl> <span data-ttu-id="d7c82-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c82-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c82-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7c82-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c82-144">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="d7c82-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




