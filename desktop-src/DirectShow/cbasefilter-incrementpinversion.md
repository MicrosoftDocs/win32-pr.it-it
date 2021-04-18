---
description: Il metodo IncremementPinVersion incrementa il numero di versione nel set di pin.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Metodo CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331543"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="ff339-103">CBaseFilter. IncrementPinVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="ff339-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="ff339-104">Il `IncremementPinVersion` metodo incrementa il numero di versione nel set di pin.</span><span class="sxs-lookup"><span data-stu-id="ff339-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff339-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff339-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="ff339-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff339-106">Parameters</span></span>

<span data-ttu-id="ff339-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ff339-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff339-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff339-108">Return value</span></span>

<span data-ttu-id="ff339-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ff339-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff339-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff339-110">Remarks</span></span>

<span data-ttu-id="ff339-111">Questo metodo incrementa la variabile membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="ff339-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="ff339-112">Se il filtro crea o Elimina in modo dinamico i pin, chiamare questo metodo ogni volta che i pin cambiano.</span><span class="sxs-lookup"><span data-stu-id="ff339-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff339-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff339-113">Requirements</span></span>



| <span data-ttu-id="ff339-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff339-114">Requirement</span></span> | <span data-ttu-id="ff339-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ff339-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff339-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff339-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ff339-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff339-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff339-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ff339-118">Library</span></span><br/> | <dl> <span data-ttu-id="ff339-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ff339-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff339-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff339-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff339-121">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ff339-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="ff339-122">**CBaseFilter::GetPinVersion**</span><span class="sxs-lookup"><span data-stu-id="ff339-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




