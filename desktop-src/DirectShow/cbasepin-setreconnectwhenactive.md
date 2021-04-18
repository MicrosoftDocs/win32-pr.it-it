---
description: Il metodo SetReconnectWhenActive specifica se il pin supporta la riconnessione dinamica.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Metodo CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324201"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="d7fbd-103">CBasePin. SetReconnectWhenActive, metodo</span><span class="sxs-lookup"><span data-stu-id="d7fbd-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="d7fbd-104">Il `SetReconnectWhenActive` metodo specifica se il pin supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7fbd-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="d7fbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7fbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7fbd-107">*bCanReconnect*</span><span class="sxs-lookup"><span data-stu-id="d7fbd-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="d7fbd-108">Valore booleano che specifica se il pin può riconnettersi dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="d7fbd-109">Se **true**, il pin può riconnettersi dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7fbd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7fbd-110">Return value</span></span>

<span data-ttu-id="d7fbd-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fbd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7fbd-112">Remarks</span></span>

<span data-ttu-id="d7fbd-113">Per impostazione predefinita, è necessario arrestare un filtro prima di riconnettere i relativi pin.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="d7fbd-114">Se il PIN è in grado di riconnettersi mentre il filtro è attivo, chiamare questo metodo con un valore **true**.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="d7fbd-115">Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="d7fbd-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fbd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7fbd-116">Requirements</span></span>



| <span data-ttu-id="d7fbd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fbd-117">Requirement</span></span> | <span data-ttu-id="d7fbd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d7fbd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fbd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7fbd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d7fbd-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fbd-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7fbd-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7fbd-121">Library</span></span><br/> | <dl> <span data-ttu-id="d7fbd-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fbd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fbd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7fbd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fbd-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d7fbd-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




