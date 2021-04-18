---
description: Il metodo NotifyFilterState invia una notifica al pin quando lo stato del filtro viene modificato.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Metodo CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331648"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="17341-103">CBaseStreamControl. NotifyFilterState, metodo</span><span class="sxs-lookup"><span data-stu-id="17341-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="17341-104">Il `NotifyFilterState` metodo invia una notifica al pin quando lo stato del filtro viene modificato.</span><span class="sxs-lookup"><span data-stu-id="17341-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="17341-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17341-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="17341-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17341-107">*nuovo \_ stato*</span><span class="sxs-lookup"><span data-stu-id="17341-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="17341-108">Specifica il nuovo stato, come membro dell'enumerazione [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="17341-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="17341-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="17341-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="17341-110">Specifica l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="17341-110">Specifies the start time.</span></span> <span data-ttu-id="17341-111">Se lo stato del nuovo filtro è \_ Running, passare il valore dal metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="17341-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="17341-112">In caso contrario, usare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="17341-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17341-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17341-113">Return value</span></span>

<span data-ttu-id="17341-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="17341-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17341-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="17341-115">Remarks</span></span>

<span data-ttu-id="17341-116">Questo metodo fa in modo che il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) interrompa l'attesa.</span><span class="sxs-lookup"><span data-stu-id="17341-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="17341-117">Chiamare questo metodo ogni volta che il filtro proprietario modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="17341-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="17341-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="17341-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="17341-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17341-119">Requirements</span></span>



| <span data-ttu-id="17341-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="17341-120">Requirement</span></span> | <span data-ttu-id="17341-121">Valore</span><span class="sxs-lookup"><span data-stu-id="17341-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17341-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17341-122">Header</span></span><br/>  | <dl> <span data-ttu-id="17341-123"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17341-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17341-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="17341-124">Library</span></span><br/> | <dl> <span data-ttu-id="17341-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17341-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17341-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17341-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17341-127">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="17341-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




