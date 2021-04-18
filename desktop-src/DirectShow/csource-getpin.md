---
description: 'Il metodo GetPin recupera un PIN. Questo metodo implementa il metodo CBaseFilter:: GetPin virtuale puro.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Metodo CSource. GetPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326936"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="317cf-104">CSource. GetPin, metodo</span><span class="sxs-lookup"><span data-stu-id="317cf-104">CSource.GetPin method</span></span>

<span data-ttu-id="317cf-105">Il `GetPin` metodo recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="317cf-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="317cf-106">Questo metodo implementa il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="317cf-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="317cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="317cf-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="317cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="317cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317cf-109">*n*</span><span class="sxs-lookup"><span data-stu-id="317cf-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="317cf-110">Numero del PIN specificato.</span><span class="sxs-lookup"><span data-stu-id="317cf-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317cf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="317cf-111">Return value</span></span>

<span data-ttu-id="317cf-112">Restituisce il puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN oppure **null** se l'indice non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="317cf-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="317cf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="317cf-113">Requirements</span></span>



| <span data-ttu-id="317cf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="317cf-114">Requirement</span></span> | <span data-ttu-id="317cf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="317cf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="317cf-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="317cf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="317cf-117"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="317cf-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="317cf-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="317cf-118">Library</span></span><br/> | <dl> <span data-ttu-id="317cf-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="317cf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317cf-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="317cf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317cf-121">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="317cf-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




