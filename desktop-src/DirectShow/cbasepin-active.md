---
description: 'Metodo CBasePin.Active: il metodo Active notifica al pin che il filtro è ora attivo.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Metodo CBasePin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096108"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="222f2-103">Metodo CBasePin.Active</span><span class="sxs-lookup"><span data-stu-id="222f2-103">CBasePin.Active method</span></span>

<span data-ttu-id="222f2-104">Il `Active` metodo notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="222f2-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="222f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="222f2-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="222f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="222f2-106">Parameters</span></span>

<span data-ttu-id="222f2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="222f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="222f2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="222f2-108">Return value</span></span>

<span data-ttu-id="222f2-109">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="222f2-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="222f2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="222f2-110">Remarks</span></span>

<span data-ttu-id="222f2-111">Quando il filtro passa da arrestato a sospeso, la [**classe CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.</span><span class="sxs-lookup"><span data-stu-id="222f2-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="222f2-112">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="222f2-112">This method does nothing in the base class.</span></span> <span data-ttu-id="222f2-113">Le classi derivate possono eseguire l'override di questo metodo. Ad esempio, un pin potrebbe eseguire il commit degli allocatori o ottenere risorse hardware.</span><span class="sxs-lookup"><span data-stu-id="222f2-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="222f2-114">Lo stato interno del gestore del grafico filtri non viene aggiornato fino a quando non viene restituita questa funzione membro, quindi non testare lo stato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="222f2-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="222f2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="222f2-115">Requirements</span></span>



| <span data-ttu-id="222f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="222f2-116">Requirement</span></span> | <span data-ttu-id="222f2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="222f2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="222f2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="222f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="222f2-119"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="222f2-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="222f2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="222f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="222f2-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="222f2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="222f2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="222f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222f2-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="222f2-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




