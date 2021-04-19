---
description: Il metodo Run notifica al pin che il filtro è ora in esecuzione.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Metodo CBasePin. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328256"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="0bcf4-103">Metodo CBasePin. Run</span><span class="sxs-lookup"><span data-stu-id="0bcf4-103">CBasePin.Run method</span></span>

<span data-ttu-id="0bcf4-104">Il `Run` metodo notifica al pin che il filtro è ora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcf4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bcf4-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="0bcf4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bcf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcf4-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="0bcf4-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0bcf4-108">Ora di inizio passata al metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bcf4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bcf4-109">Return value</span></span>

<span data-ttu-id="0bcf4-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcf4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bcf4-111">Remarks</span></span>

<span data-ttu-id="0bcf4-112">Quando il filtro passa da sospeso a in esecuzione, la classe [**CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin del filtro.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="0bcf4-113">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-113">This method does nothing in the base class.</span></span> <span data-ttu-id="0bcf4-114">Classi derivate possono eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-114">Derived classes can override this method.</span></span> <span data-ttu-id="0bcf4-115">Ad esempio, un PIN potrebbe avviare un thread di lavoro che fornisce esempi.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="0bcf4-116">Lo stato interno del gestore del grafico del filtro non viene aggiornato finché la funzione membro non viene restituita, pertanto non è necessario eseguire il test dello stato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcf4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bcf4-117">Requirements</span></span>



| <span data-ttu-id="0bcf4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bcf4-118">Requirement</span></span> | <span data-ttu-id="0bcf4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0bcf4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcf4-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0bcf4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0bcf4-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf4-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0bcf4-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="0bcf4-122">Library</span></span><br/> | <dl> <span data-ttu-id="0bcf4-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bcf4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bcf4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcf4-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="0bcf4-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




