---
description: "Il metodo run esegue l'oggetto. Questo metodo implementa il metodo IMediaFilter:: Run."
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Metodo CBaseMediaFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325075"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="1a735-104">Metodo CBaseMediaFilter. Run</span><span class="sxs-lookup"><span data-stu-id="1a735-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="1a735-105">Il `Run` metodo esegue l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a735-105">The `Run` method runs the object.</span></span> <span data-ttu-id="1a735-106">Questo metodo implementa il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="1a735-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a735-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a735-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="1a735-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a735-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="1a735-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1a735-110">Tempo di riferimento corrispondente all'ora del flusso 0.</span><span class="sxs-lookup"><span data-stu-id="1a735-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a735-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a735-111">Return value</span></span>

<span data-ttu-id="1a735-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a735-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a735-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a735-113">Remarks</span></span>

<span data-ttu-id="1a735-114">Se l'oggetto viene arrestato, questo metodo sospende l'oggetto chiamando il metodo [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="1a735-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="1a735-115">Imposta quindi la variabile membro di [**\_ stato CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) sullo stato \_ in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1a735-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="1a735-116">Il tempo di flusso viene calcolato come ora di riferimento corrente meno *tStart*.</span><span class="sxs-lookup"><span data-stu-id="1a735-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="1a735-117">È necessario eseguire il rendering di un campione multimediale con un timestamp di zero all'ora *tStart*.</span><span class="sxs-lookup"><span data-stu-id="1a735-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a735-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a735-118">Requirements</span></span>



| <span data-ttu-id="1a735-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a735-119">Requirement</span></span> | <span data-ttu-id="1a735-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1a735-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a735-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a735-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1a735-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a735-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a735-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a735-123">Library</span></span><br/> | <dl> <span data-ttu-id="1a735-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a735-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a735-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a735-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a735-126">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="1a735-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




