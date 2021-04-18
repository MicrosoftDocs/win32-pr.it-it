---
description: Il metodo IsEndOfStreamDelivered esegue una query per determinare se l' \_ evento EC complete è stato recapitato al gestore del grafico dei filtri.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Metodo CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330053"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a><span data-ttu-id="59eb4-103">CBaseRenderer. IsEndOfStreamDelivered, metodo</span><span class="sxs-lookup"><span data-stu-id="59eb4-103">CBaseRenderer.IsEndOfStreamDelivered method</span></span>

<span data-ttu-id="59eb4-104">Il `IsEndOfStreamDelivered` metodo esegue una query che indica se l' \_ evento di completamento EC è stato recapitato al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="59eb4-104">The `IsEndOfStreamDelivered` method queries whether the EC\_COMPLETE event has been delivered to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eb4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59eb4-105">Syntax</span></span>


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a><span data-ttu-id="59eb4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59eb4-106">Parameters</span></span>

<span data-ttu-id="59eb4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="59eb4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59eb4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59eb4-108">Return value</span></span>

<span data-ttu-id="59eb4-109">Restituisce il flag [**CBaseRenderer:: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .</span><span class="sxs-lookup"><span data-stu-id="59eb4-109">Returns the [**CBaseRenderer::m\_bEOSDelivered**](cbaserenderer-m-beosdelivered.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eb4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59eb4-110">Requirements</span></span>



| <span data-ttu-id="59eb4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="59eb4-111">Requirement</span></span> | <span data-ttu-id="59eb4-112">Valore</span><span class="sxs-lookup"><span data-stu-id="59eb4-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59eb4-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59eb4-113">Header</span></span><br/>  | <dl> <span data-ttu-id="59eb4-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59eb4-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59eb4-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="59eb4-115">Library</span></span><br/> | <dl> <span data-ttu-id="59eb4-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59eb4-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eb4-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59eb4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eb4-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="59eb4-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




