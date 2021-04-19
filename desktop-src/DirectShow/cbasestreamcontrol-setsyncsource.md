---
description: Il metodo SetSyncSource notifica alla classe di base il clock di riferimento corrente.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Metodo CBaseStreamControl. SetSyncSource (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324030"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="867f9-103">CBaseStreamControl. SetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="867f9-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="867f9-104">Il `SetSyncSource` metodo notifica alla classe di base l'orologio di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="867f9-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="867f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="867f9-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="867f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="867f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867f9-107">*pRefClock*</span><span class="sxs-lookup"><span data-stu-id="867f9-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="867f9-108">Puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) dell'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="867f9-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867f9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="867f9-109">Return value</span></span>

<span data-ttu-id="867f9-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="867f9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="867f9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="867f9-111">Remarks</span></span>

<span data-ttu-id="867f9-112">Chiamare questo metodo dall'interno del metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro.</span><span class="sxs-lookup"><span data-stu-id="867f9-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="867f9-113">La classe **CBaseStreamControl** usa l'interfaccia **IReferenceClock** per assicurarsi che non elimini troppo rapidamente i campioni.</span><span class="sxs-lookup"><span data-stu-id="867f9-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="867f9-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="867f9-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="867f9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="867f9-115">Requirements</span></span>



| <span data-ttu-id="867f9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="867f9-116">Requirement</span></span> | <span data-ttu-id="867f9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="867f9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867f9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="867f9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="867f9-119"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="867f9-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="867f9-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="867f9-120">Library</span></span><br/> | <dl> <span data-ttu-id="867f9-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="867f9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867f9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="867f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867f9-123">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="867f9-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




