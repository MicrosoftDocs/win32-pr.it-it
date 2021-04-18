---
description: Il metodo CanReconnectWhenActive esegue una query se il pin supporta la riconnessione dinamica.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Metodo CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330859"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="d444f-103">CBasePin. CanReconnectWhenActive, metodo</span><span class="sxs-lookup"><span data-stu-id="d444f-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="d444f-104">Il `CanReconnectWhenActive` metodo esegue una query se il pin supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="d444f-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="d444f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d444f-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="d444f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d444f-106">Parameters</span></span>

<span data-ttu-id="d444f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d444f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d444f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d444f-108">Return value</span></span>

<span data-ttu-id="d444f-109">Restituisce un valore booleano che specifica se il PIN è in grado di riconnettersi dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d444f-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="d444f-110">Se **true**, il pin può riconnettersi dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d444f-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="d444f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d444f-111">Remarks</span></span>

<span data-ttu-id="d444f-112">Per impostazione predefinita, è necessario arrestare un filtro prima di riconnettere i relativi pin.</span><span class="sxs-lookup"><span data-stu-id="d444f-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="d444f-113">Se un pin supporta la riconnessione dinamica, tuttavia, può riconnettersi mentre il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="d444f-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="d444f-114">Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="d444f-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d444f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d444f-115">Requirements</span></span>



| <span data-ttu-id="d444f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d444f-116">Requirement</span></span> | <span data-ttu-id="d444f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d444f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d444f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d444f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d444f-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d444f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d444f-120">Library</span></span><br/> | <dl> <span data-ttu-id="d444f-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d444f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d444f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d444f-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d444f-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




