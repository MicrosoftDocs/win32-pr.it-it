---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin:: EndOfStream. Chiamare questo metodo solo sui pin di input.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Metodo CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332768"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="fa23c-105">CBasePin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="fa23c-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="fa23c-106">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fa23c-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="fa23c-107">Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="fa23c-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="fa23c-108">Chiamare questo metodo solo sui pin di input.</span><span class="sxs-lookup"><span data-stu-id="fa23c-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa23c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa23c-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="fa23c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa23c-110">Parameters</span></span>

<span data-ttu-id="fa23c-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fa23c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa23c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa23c-112">Return value</span></span>

<span data-ttu-id="fa23c-113">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa23c-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa23c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa23c-114">Remarks</span></span>

<span data-ttu-id="fa23c-115">Il filtro deve passare le notifiche di fine flusso downstream ai pin di input dei filtri connessi.</span><span class="sxs-lookup"><span data-stu-id="fa23c-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="fa23c-116">Se il filtro è un renderer, deve inviare una notifica di evento [**EC \_ completo**](ec-complete.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="fa23c-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="fa23c-117">Per altre informazioni, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="fa23c-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="fa23c-118">Nella classe di base, questo metodo non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="fa23c-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="fa23c-119">Le classi derivate devono eseguire l'override del metodo.</span><span class="sxs-lookup"><span data-stu-id="fa23c-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa23c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa23c-120">Requirements</span></span>



| <span data-ttu-id="fa23c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa23c-121">Requirement</span></span> | <span data-ttu-id="fa23c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fa23c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa23c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa23c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fa23c-124"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa23c-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fa23c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa23c-125">Library</span></span><br/> | <dl> <span data-ttu-id="fa23c-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fa23c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa23c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa23c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa23c-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="fa23c-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




