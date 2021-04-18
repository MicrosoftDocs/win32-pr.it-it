---
description: Il metodo GetPinCount Recupera il numero di pin.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Metodo CBaseFilter. GetPinCount (Amfilter. h)
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331553"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="f283f-103">CBaseFilter. GetPinCount, metodo</span><span class="sxs-lookup"><span data-stu-id="f283f-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="f283f-104">Il `GetPinCount` metodo recupera il numero di pin.</span><span class="sxs-lookup"><span data-stu-id="f283f-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="f283f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f283f-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="f283f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f283f-106">Parameters</span></span>

<span data-ttu-id="f283f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f283f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f283f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f283f-108">Return value</span></span>

<span data-ttu-id="f283f-109">Restituisce il numero di pin.</span><span class="sxs-lookup"><span data-stu-id="f283f-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="f283f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f283f-110">Remarks</span></span>

<span data-ttu-id="f283f-111">La classe derivata deve implementare questo metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="f283f-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="f283f-112">Restituisce il numero di PIN attualmente disponibili in questo filtro.</span><span class="sxs-lookup"><span data-stu-id="f283f-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="f283f-113">I filtri possono creare o eliminare in modo dinamico i pin.</span><span class="sxs-lookup"><span data-stu-id="f283f-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="f283f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f283f-114">Requirements</span></span>



| <span data-ttu-id="f283f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f283f-115">Requirement</span></span> | <span data-ttu-id="f283f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f283f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f283f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f283f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f283f-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f283f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f283f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f283f-119">Library</span></span><br/> | <dl> <span data-ttu-id="f283f-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f283f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f283f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f283f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f283f-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f283f-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




