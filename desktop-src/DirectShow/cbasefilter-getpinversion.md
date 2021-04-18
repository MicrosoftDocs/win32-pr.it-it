---
description: Il metodo GetPinVersion recupera un numero di versione per il set di pin in questo filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Metodo CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331549"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="d5639-103">CBaseFilter. GetPinVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="d5639-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="d5639-104">Il `GetPinVersion` metodo recupera un numero di versione per il set di pin in questo filtro.</span><span class="sxs-lookup"><span data-stu-id="d5639-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5639-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5639-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="d5639-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5639-106">Parameters</span></span>

<span data-ttu-id="d5639-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d5639-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5639-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5639-108">Return value</span></span>

<span data-ttu-id="d5639-109">Restituisce la variabile membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="d5639-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5639-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5639-110">Remarks</span></span>

<span data-ttu-id="d5639-111">Il costruttore **CBaseFilter** Inizializza la versione del pin su 1.</span><span class="sxs-lookup"><span data-stu-id="d5639-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="d5639-112">Nella classe base questo numero non viene mai modificato.</span><span class="sxs-lookup"><span data-stu-id="d5639-112">In the base class, this number never changes.</span></span> <span data-ttu-id="d5639-113">Se il filtro crea o Elimina in modo dinamico i pin, è necessario incrementare la versione del PIN ogni volta che i pin cambiano.</span><span class="sxs-lookup"><span data-stu-id="d5639-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="d5639-114">Per incrementare il numero di versione, chiamare il metodo [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="d5639-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="d5639-115">L'oggetto enumeratore pin, implementato dalla classe [**CEnumPins**](cenumpins.md) , usa la versione pin per mantenersi sincronizzata con il filtro.</span><span class="sxs-lookup"><span data-stu-id="d5639-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5639-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5639-116">Requirements</span></span>



| <span data-ttu-id="d5639-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5639-117">Requirement</span></span> | <span data-ttu-id="d5639-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d5639-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5639-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5639-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d5639-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5639-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5639-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5639-121">Library</span></span><br/> | <dl> <span data-ttu-id="d5639-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5639-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5639-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5639-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5639-124">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d5639-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




