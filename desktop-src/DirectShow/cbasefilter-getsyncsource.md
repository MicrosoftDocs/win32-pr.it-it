---
description: "Il metodo GetSyncSource recupera l'orologio di riferimento utilizzato dal filtro. Questo metodo implementa il metodo IMediaFilter:: GetSyncSource."
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Metodo CBaseFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331544"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="34493-104">CBaseFilter. GetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="34493-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="34493-105">Il `GetSyncSource` metodo recupera l'orologio di riferimento utilizzato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="34493-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="34493-106">Questo metodo implementa il metodo [**IMediaFilter:: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="34493-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34493-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34493-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="34493-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="34493-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34493-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="34493-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="34493-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del clock.</span><span class="sxs-lookup"><span data-stu-id="34493-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34493-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34493-111">Return value</span></span>

<span data-ttu-id="34493-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="34493-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="34493-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="34493-113">Remarks</span></span>

<span data-ttu-id="34493-114">Se il filtro non usa un clock di riferimento, *\* pClock* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="34493-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="34493-115">Quando il metodo restituisce un risultato, se *\* pClock* è diverso da **null**, l'interfaccia **IReferenceClock** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="34493-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="34493-116">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="34493-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="34493-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34493-117">Requirements</span></span>



| <span data-ttu-id="34493-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34493-118">Requirement</span></span> | <span data-ttu-id="34493-119">Valore</span><span class="sxs-lookup"><span data-stu-id="34493-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34493-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34493-120">Header</span></span><br/>  | <dl> <span data-ttu-id="34493-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34493-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="34493-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="34493-122">Library</span></span><br/> | <dl> <span data-ttu-id="34493-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34493-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34493-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34493-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34493-125">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="34493-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




