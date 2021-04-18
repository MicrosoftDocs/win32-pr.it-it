---
description: "Il metodo SetSyncSource imposta un clock di riferimento per l'oggetto. Questo metodo implementa il metodo IMediaFilter:: SetSyncSource."
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Metodo CBaseMediaFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325072"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="c538a-104">CBaseMediaFilter. SetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="c538a-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="c538a-105">Il `SetSyncSource` metodo imposta un clock di riferimento per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c538a-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="c538a-106">Questo metodo implementa il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="c538a-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c538a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c538a-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="c538a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c538a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c538a-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="c538a-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="c538a-110">Puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) dell'orologio o **null**.</span><span class="sxs-lookup"><span data-stu-id="c538a-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c538a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c538a-111">Return value</span></span>

<span data-ttu-id="c538a-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c538a-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c538a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c538a-113">Requirements</span></span>



| <span data-ttu-id="c538a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c538a-114">Requirement</span></span> | <span data-ttu-id="c538a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c538a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c538a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c538a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c538a-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c538a-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c538a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c538a-118">Library</span></span><br/> | <dl> <span data-ttu-id="c538a-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c538a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c538a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c538a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c538a-121">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="c538a-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




