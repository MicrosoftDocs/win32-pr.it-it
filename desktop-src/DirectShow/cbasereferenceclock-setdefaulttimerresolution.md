---
description: Il metodo SetDefaultTimerResolution imposta la risoluzione del timer del clock di riferimento.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Metodo CBaseReferenceClock. SetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332225"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="e2483-103">CBaseReferenceClock. SetDefaultTimerResolution, metodo</span><span class="sxs-lookup"><span data-stu-id="e2483-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="e2483-104">Il `SetDefaultTimerResolution` metodo imposta la risoluzione del timer del clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="e2483-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2483-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2483-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="e2483-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2483-107">*timerResolution*</span><span class="sxs-lookup"><span data-stu-id="e2483-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="e2483-108">Risoluzione minima del timer, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="e2483-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="e2483-109">Se il valore è zero, l'orologio di riferimento Annulla la richiesta precedente.</span><span class="sxs-lookup"><span data-stu-id="e2483-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2483-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2483-110">Return value</span></span>

<span data-ttu-id="e2483-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2483-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2483-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2483-112">Remarks</span></span>

<span data-ttu-id="e2483-113">Questo metodo implementa il metodo [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="e2483-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2483-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2483-114">Requirements</span></span>



| <span data-ttu-id="e2483-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2483-115">Requirement</span></span> | <span data-ttu-id="e2483-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e2483-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2483-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2483-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e2483-118"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2483-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2483-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2483-119">Library</span></span><br/> | <dl> <span data-ttu-id="e2483-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e2483-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2483-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2483-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2483-122">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="e2483-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




