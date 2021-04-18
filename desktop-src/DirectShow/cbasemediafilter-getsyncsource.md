---
description: "Il metodo GetSyncSource recupera l'orologio di riferimento usato dall'oggetto. Questo metodo implementa il metodo IMediaFilter:: GetSyncSource."
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Metodo CBaseMediaFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325380"
---
# <a name="cbasemediafiltergetsyncsource-method"></a><span data-ttu-id="a1a8c-104">CBaseMediaFilter. GetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="a1a8c-104">CBaseMediaFilter.GetSyncSource method</span></span>

<span data-ttu-id="a1a8c-105">Il `GetSyncSource` metodo recupera l'orologio di riferimento usato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1a8c-105">The `GetSyncSource` method retrieves the reference clock that the object is using.</span></span> <span data-ttu-id="a1a8c-106">Questo metodo implementa il metodo [**IMediaFilter:: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="a1a8c-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a8c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1a8c-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="a1a8c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1a8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a8c-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="a1a8c-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="a1a8c-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del clock.</span><span class="sxs-lookup"><span data-stu-id="a1a8c-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a8c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1a8c-111">Return value</span></span>

<span data-ttu-id="a1a8c-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="a1a8c-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a8c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1a8c-113">Remarks</span></span>

<span data-ttu-id="a1a8c-114">Se l'oggetto non usa un clock di riferimento, *\* pClock* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1a8c-114">If the object is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="a1a8c-115">Quando il metodo restituisce un risultato, se *\* pClock* è diverso da **null**, l'interfaccia **IReferenceClock** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="a1a8c-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="a1a8c-116">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1a8c-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a8c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1a8c-117">Requirements</span></span>



| <span data-ttu-id="a1a8c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a8c-118">Requirement</span></span> | <span data-ttu-id="a1a8c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a1a8c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a8c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1a8c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a8c-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8c-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a1a8c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1a8c-122">Library</span></span><br/> | <dl> <span data-ttu-id="a1a8c-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1a8c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1a8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a8c-125">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="a1a8c-125">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




