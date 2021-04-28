---
description: 'Metodo CBaseFilter.GetPinCount: il metodo GetPinCount recupera il numero di pin.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Metodo CBaseFilter.GetPinCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099789"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="a7841-103">Metodo CBaseFilter.GetPinCount</span><span class="sxs-lookup"><span data-stu-id="a7841-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="a7841-104">Il `GetPinCount` metodo recupera il numero di pin.</span><span class="sxs-lookup"><span data-stu-id="a7841-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7841-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7841-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a7841-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7841-106">Parameters</span></span>

<span data-ttu-id="a7841-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a7841-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7841-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7841-108">Return value</span></span>

<span data-ttu-id="a7841-109">Restituisce il numero di pin.</span><span class="sxs-lookup"><span data-stu-id="a7841-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7841-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7841-110">Remarks</span></span>

<span data-ttu-id="a7841-111">La classe derivata deve implementare questo metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="a7841-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="a7841-112">Restituisce il numero di pin attualmente disponibili per questo filtro.</span><span class="sxs-lookup"><span data-stu-id="a7841-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="a7841-113">I filtri possono creare o eliminare in modo dinamico i pin.</span><span class="sxs-lookup"><span data-stu-id="a7841-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7841-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7841-114">Requirements</span></span>



| <span data-ttu-id="a7841-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7841-115">Requirement</span></span> | <span data-ttu-id="a7841-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a7841-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7841-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7841-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a7841-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7841-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a7841-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7841-119">Library</span></span><br/> | <dl> <span data-ttu-id="a7841-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a7841-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7841-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7841-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7841-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a7841-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




