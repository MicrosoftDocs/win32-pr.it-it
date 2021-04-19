---
description: "Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo esegue l'override del Metodo CBasePin:: EndOfStream."
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Metodo CRendererInputPin. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333185"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="a8ba2-104">CRendererInputPin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="a8ba2-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="a8ba2-105">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="a8ba2-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="a8ba2-106">Questo metodo esegue l'override del metodo [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ba2-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ba2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8ba2-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="a8ba2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8ba2-108">Parameters</span></span>

<span data-ttu-id="a8ba2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8ba2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8ba2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8ba2-110">Return value</span></span>

<span data-ttu-id="a8ba2-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8ba2-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ba2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8ba2-112">Requirements</span></span>



| <span data-ttu-id="a8ba2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ba2-113">Requirement</span></span> | <span data-ttu-id="a8ba2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a8ba2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ba2-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8ba2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ba2-116"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ba2-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8ba2-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8ba2-117">Library</span></span><br/> | <dl> <span data-ttu-id="a8ba2-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ba2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ba2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8ba2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ba2-120">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="a8ba2-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




