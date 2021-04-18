---
description: Il metodo GetState recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Metodo CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325928"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="2287a-103">Metodo CBaseRenderer. GetState</span><span class="sxs-lookup"><span data-stu-id="2287a-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="2287a-104">Il `GetState` metodo recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).</span><span class="sxs-lookup"><span data-stu-id="2287a-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="2287a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2287a-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="2287a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2287a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2287a-107">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="2287a-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="2287a-108">Intervallo di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2287a-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2287a-109">*State*</span><span class="sxs-lookup"><span data-stu-id="2287a-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="2287a-110">Puntatore a una variabile che riceve un membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="2287a-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2287a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2287a-111">Return value</span></span>

<span data-ttu-id="2287a-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2287a-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2287a-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2287a-113">Return code</span></span>                                                                                                | <span data-ttu-id="2287a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2287a-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="2287a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2287a-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2287a-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2287a-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2287a-117"><dt>**\_ \_ stato \_ INTERmedio di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="2287a-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="2287a-118">Il filtro sta passando allo stato indicato.</span><span class="sxs-lookup"><span data-stu-id="2287a-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="2287a-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2287a-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="2287a-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="2287a-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="2287a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2287a-121">Remarks</span></span>

<span data-ttu-id="2287a-122">Questo metodo esegue l'override del metodo [**CBaseFilter:: GetState**](cbasefilter-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="2287a-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="2287a-123">Quando il renderer viene sospeso, non viene completata la transizione di stato fino a quando non viene ricevuto un campione per il rendering.</span><span class="sxs-lookup"><span data-stu-id="2287a-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="2287a-124">Se il timeout scade prima del completamento della transizione di stato, il metodo restituisce l' \_ \_ intermediario dello stato VFW S \_ .</span><span class="sxs-lookup"><span data-stu-id="2287a-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2287a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2287a-125">Requirements</span></span>



| <span data-ttu-id="2287a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2287a-126">Requirement</span></span> | <span data-ttu-id="2287a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2287a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2287a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2287a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2287a-129"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2287a-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2287a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="2287a-130">Library</span></span><br/> | <dl> <span data-ttu-id="2287a-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2287a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2287a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2287a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2287a-133">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2287a-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




