---
description: 'Il metodo run esegue il filtro. Questo metodo implementa il metodo IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Metodo CBaseFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326941"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="4e3c7-104">Metodo CBaseFilter. Run</span><span class="sxs-lookup"><span data-stu-id="4e3c7-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="4e3c7-105">Il `Run` metodo esegue il filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="4e3c7-106">Questo metodo implementa il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="4e3c7-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e3c7-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="4e3c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e3c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3c7-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="4e3c7-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4e3c7-110">Tempo di riferimento corrispondente all'ora del flusso 0.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e3c7-111">Return value</span></span>

<span data-ttu-id="4e3c7-112">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3c7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e3c7-113">Remarks</span></span>

<span data-ttu-id="4e3c7-114">Se il filtro viene arrestato, questo metodo sospende il filtro chiamando il metodo [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="4e3c7-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="4e3c7-115">Chiama quindi il metodo [**CBasePin:: Run**](cbasepin-run.md) su ognuno dei pin connessi del filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="4e3c7-116">Infine, imposta la variabile membro di [**\_ stato CBaseFilter:: m**](cbasefilter-m-state.md) sullo stato \_ in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="4e3c7-117">Il tempo di flusso viene calcolato come ora di riferimento corrente meno *tStart*.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="4e3c7-118">È necessario eseguire il rendering di un campione multimediale con un timestamp di zero all'ora *tStart*.</span><span class="sxs-lookup"><span data-stu-id="4e3c7-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3c7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e3c7-119">Requirements</span></span>



| <span data-ttu-id="4e3c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e3c7-120">Requirement</span></span> | <span data-ttu-id="4e3c7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4e3c7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3c7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e3c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4e3c7-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3c7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e3c7-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e3c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="4e3c7-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3c7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3c7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e3c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3c7-127">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4e3c7-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




