---
description: "Il metodo GetState recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo IMediaFilter:: GetState."
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Metodo CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325382"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="f9af4-104">Metodo CBaseMediaFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="f9af4-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="f9af4-105">Il `GetState` metodo recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso).</span><span class="sxs-lookup"><span data-stu-id="f9af4-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="f9af4-106">Questo metodo implementa il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="f9af4-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9af4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9af4-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="f9af4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9af4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9af4-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="f9af4-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="f9af4-110">Intervallo di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f9af4-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f9af4-111">*State*</span><span class="sxs-lookup"><span data-stu-id="f9af4-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="f9af4-112">Puntatore a una variabile che riceve un membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9af4-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9af4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9af4-113">Return value</span></span>

<span data-ttu-id="f9af4-114">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="f9af4-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9af4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9af4-115">Remarks</span></span>

<span data-ttu-id="f9af4-116">Nella classe di base tutte le transizioni di stato sono sincrone e il parametro *dwMilliSecsTimeout* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f9af4-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="f9af4-117">Se una classe derivata esegue transizioni di stato asincrone, deve eseguire l'override di questo metodo per attendere durante le transizioni di stato, con un timeout di *dwMilliSecsTimeout* millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f9af4-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9af4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9af4-118">Requirements</span></span>



| <span data-ttu-id="f9af4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9af4-119">Requirement</span></span> | <span data-ttu-id="f9af4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f9af4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9af4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9af4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f9af4-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9af4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9af4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9af4-123">Library</span></span><br/> | <dl> <span data-ttu-id="f9af4-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9af4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9af4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9af4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9af4-126">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="f9af4-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




