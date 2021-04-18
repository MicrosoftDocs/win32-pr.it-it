---
description: 'Il metodo GetState recupera lo stato dei filtri (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo IMediaFilter:: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Metodo CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331545"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="4323f-104">Metodo CBaseFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="4323f-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="4323f-105">Il `GetState` metodo recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).</span><span class="sxs-lookup"><span data-stu-id="4323f-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="4323f-106">Questo metodo implementa il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="4323f-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4323f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4323f-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="4323f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4323f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4323f-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="4323f-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="4323f-110">Intervallo di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="4323f-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4323f-111">*State*</span><span class="sxs-lookup"><span data-stu-id="4323f-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="4323f-112">Puntatore a una variabile che riceve un membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="4323f-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4323f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4323f-113">Return value</span></span>

<span data-ttu-id="4323f-114">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="4323f-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4323f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4323f-115">Remarks</span></span>

<span data-ttu-id="4323f-116">Nella classe di base tutte le transizioni di stato sono sincrone e il parametro *dwMilliSecsTimeout* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4323f-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="4323f-117">Se una classe derivata esegue transizioni di stato asincrone, deve eseguire l'override di questo metodo per attendere durante le transizioni di stato, con un timeout di *dwMilliSecsTimeout* millisecondi.</span><span class="sxs-lookup"><span data-stu-id="4323f-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="4323f-118">Se il filtro non recapita i dati mentre è in pausa, eseguire l'override del `GetState` metodo per restituire il valore del cant del valore di VFW \_ \_ \_ quando il filtro è sospeso (vedere la pagina relativa alla [distribuzione di esempi](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="4323f-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="4323f-119">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4323f-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="4323f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4323f-120">Requirements</span></span>



| <span data-ttu-id="4323f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4323f-121">Requirement</span></span> | <span data-ttu-id="4323f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4323f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4323f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4323f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4323f-124"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4323f-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4323f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4323f-125">Library</span></span><br/> | <dl> <span data-ttu-id="4323f-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4323f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4323f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4323f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4323f-128">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4323f-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




