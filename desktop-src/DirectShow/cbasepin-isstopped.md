---
description: Il metodo arrestato determina se il filtro contenente questo pin è stato arrestato.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Metodo CBasePin. Stopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332874"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="55e32-103">Metodo CBasePin. Stopped</span><span class="sxs-lookup"><span data-stu-id="55e32-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="55e32-104">Il `IsStopped` metodo determina se il filtro contenente questo pin è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="55e32-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55e32-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="55e32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55e32-106">Parameters</span></span>

<span data-ttu-id="55e32-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="55e32-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55e32-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55e32-108">Return value</span></span>

<span data-ttu-id="55e32-109">Restituisce **true** se il filtro è arrestato.</span><span class="sxs-lookup"><span data-stu-id="55e32-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="55e32-110">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="55e32-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e32-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="55e32-111">Remarks</span></span>

<span data-ttu-id="55e32-112">Non chiamare questo metodo dall'interno del metodo del costruttore **CBasePin** , perché il filtro potrebbe non essere ancora inizializzato.</span><span class="sxs-lookup"><span data-stu-id="55e32-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e32-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55e32-113">Requirements</span></span>



| <span data-ttu-id="55e32-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="55e32-114">Requirement</span></span> | <span data-ttu-id="55e32-115">Valore</span><span class="sxs-lookup"><span data-stu-id="55e32-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e32-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55e32-116">Header</span></span><br/>  | <dl> <span data-ttu-id="55e32-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55e32-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55e32-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="55e32-118">Library</span></span><br/> | <dl> <span data-ttu-id="55e32-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="55e32-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e32-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55e32-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e32-121">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="55e32-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




