---
description: Il metodo SetTimeDelta regola l'ora di clock interna.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Metodo CBaseReferenceClock. SetTimeDelta (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332220"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="82b66-103">CBaseReferenceClock. SetTimeDelta, metodo</span><span class="sxs-lookup"><span data-stu-id="82b66-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="82b66-104">Il `SetTimeDelta` metodo regola l'ora di clock interna.</span><span class="sxs-lookup"><span data-stu-id="82b66-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b66-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82b66-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="82b66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82b66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b66-107">*TimeDelta* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="82b66-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="82b66-108">Valore che consente di regolare l'ora di clock, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="82b66-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="82b66-109">Un valore positivo consente di spostare l'orologio avanti e un valore negativo consente di spostare l'orologio indietro.</span><span class="sxs-lookup"><span data-stu-id="82b66-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b66-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82b66-110">Return value</span></span>

<span data-ttu-id="82b66-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82b66-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="82b66-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="82b66-112">Remarks</span></span>

<span data-ttu-id="82b66-113">La classe derivata può utilizzare questo metodo per modificare il clock interno, se deriva dal dispositivo che fornisce informazioni sulla tempistica.</span><span class="sxs-lookup"><span data-stu-id="82b66-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="82b66-114">Il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) restituisce mai valori decrescenti.</span><span class="sxs-lookup"><span data-stu-id="82b66-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="82b66-115">Se si imposta l'orologio indietro, **getTime** restituisce il valore precedente fino a quando l'orologio raggiunge nuovamente tale valore.</span><span class="sxs-lookup"><span data-stu-id="82b66-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b66-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82b66-116">Requirements</span></span>



| <span data-ttu-id="82b66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b66-117">Requirement</span></span> | <span data-ttu-id="82b66-118">Valore</span><span class="sxs-lookup"><span data-stu-id="82b66-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b66-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82b66-119">Header</span></span><br/>  | <dl> <span data-ttu-id="82b66-120"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82b66-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="82b66-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="82b66-121">Library</span></span><br/> | <dl> <span data-ttu-id="82b66-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82b66-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b66-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82b66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b66-124">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="82b66-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




