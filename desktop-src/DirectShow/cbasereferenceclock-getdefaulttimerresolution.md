---
description: Il metodo GetDefaultTimerResolution restituisce la risoluzione corrente del timer del clock di riferimento.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Metodo CBaseReferenceClock. GetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328033"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="7e76c-103">CBaseReferenceClock. GetDefaultTimerResolution, metodo</span><span class="sxs-lookup"><span data-stu-id="7e76c-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="7e76c-104">Il `GetDefaultTimerResolution` metodo restituisce la risoluzione corrente del timer del clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7e76c-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e76c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e76c-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="7e76c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e76c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e76c-107">*pTimerResolution*</span><span class="sxs-lookup"><span data-stu-id="7e76c-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="7e76c-108">Riceve la risoluzione del timer richiesta, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="7e76c-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e76c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e76c-109">Return value</span></span>

<span data-ttu-id="7e76c-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e76c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e76c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e76c-111">Remarks</span></span>

<span data-ttu-id="7e76c-112">Questo metodo implementa il metodo [**IReferenceClockTimerControl:: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="7e76c-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e76c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e76c-113">Requirements</span></span>



| <span data-ttu-id="7e76c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e76c-114">Requirement</span></span> | <span data-ttu-id="7e76c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7e76c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e76c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e76c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7e76c-117"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e76c-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e76c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e76c-118">Library</span></span><br/> | <dl> <span data-ttu-id="7e76c-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7e76c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e76c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e76c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e76c-121">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="7e76c-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




