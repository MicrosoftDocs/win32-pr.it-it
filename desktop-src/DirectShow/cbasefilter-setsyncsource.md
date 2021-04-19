---
description: 'Il metodo SetSyncSource imposta un clock di riferimento per il filtro. Questo metodo implementa il metodo IMediaFilter:: SetSyncSource.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Metodo CBaseFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331659"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="04d0c-104">CBaseFilter. SetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="04d0c-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="04d0c-105">Il metodo **SetSyncSource** imposta un clock di riferimento per il filtro.</span><span class="sxs-lookup"><span data-stu-id="04d0c-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="04d0c-106">Questo metodo implementa il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="04d0c-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d0c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d0c-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="04d0c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04d0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d0c-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="04d0c-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="04d0c-110">Puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) dell'orologio o **null**.</span><span class="sxs-lookup"><span data-stu-id="04d0c-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d0c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04d0c-111">Return value</span></span>

<span data-ttu-id="04d0c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04d0c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04d0c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04d0c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d0c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04d0c-114">Requirements</span></span>



| <span data-ttu-id="04d0c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d0c-115">Requirement</span></span> | <span data-ttu-id="04d0c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="04d0c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d0c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04d0c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="04d0c-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04d0c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04d0c-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="04d0c-119">Library</span></span><br/> | <dl> <span data-ttu-id="04d0c-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="04d0c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d0c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04d0c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d0c-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="04d0c-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




