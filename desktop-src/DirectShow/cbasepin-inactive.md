---
description: Il metodo inattivo notifica al pin che il filtro non è più attivo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Metodo CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329538"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="11640-103">Metodo CBasePin. Inactive</span><span class="sxs-lookup"><span data-stu-id="11640-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="11640-104">Il `Inactive` metodo notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="11640-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="11640-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11640-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="11640-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11640-106">Parameters</span></span>

<span data-ttu-id="11640-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="11640-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11640-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11640-108">Return value</span></span>

<span data-ttu-id="11640-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11640-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="11640-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="11640-110">Remarks</span></span>

<span data-ttu-id="11640-111">Quando il filtro viene arrestato, la classe [**CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.</span><span class="sxs-lookup"><span data-stu-id="11640-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="11640-112">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="11640-112">This method does nothing in the base class.</span></span> <span data-ttu-id="11640-113">Le classi derivate devono eseguire l'override di questo metodo per liberare tutte le risorse ottenute dal metodo [**CBasePin:: Active**](cbasepin-active.md) ; ad esempio, per decommitre gli allocatori del PIN.</span><span class="sxs-lookup"><span data-stu-id="11640-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="11640-114">Lo stato interno del gestore del grafico del filtro non viene aggiornato finché il metodo non viene restituito, pertanto non è necessario eseguire il test dello stato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="11640-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="11640-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11640-115">Requirements</span></span>



| <span data-ttu-id="11640-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="11640-116">Requirement</span></span> | <span data-ttu-id="11640-117">Valore</span><span class="sxs-lookup"><span data-stu-id="11640-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11640-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11640-118">Header</span></span><br/>  | <dl> <span data-ttu-id="11640-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11640-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="11640-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="11640-120">Library</span></span><br/> | <dl> <span data-ttu-id="11640-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11640-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11640-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11640-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11640-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="11640-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




