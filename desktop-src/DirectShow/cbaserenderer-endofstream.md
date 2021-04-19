---
description: Il metodo EndOfStream notifica al filtro che il pin di input ha ricevuto una notifica di fine del flusso.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Metodo CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329384"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="52c49-103">CBaseRenderer. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="52c49-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="52c49-104">Il `EndOfStream` metodo notifica al filtro che il pin di input ha ricevuto una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="52c49-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c49-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52c49-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="52c49-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52c49-106">Parameters</span></span>

<span data-ttu-id="52c49-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="52c49-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52c49-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52c49-108">Return value</span></span>

<span data-ttu-id="52c49-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52c49-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c49-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c49-110">Remarks</span></span>

<span data-ttu-id="52c49-111">Il pin di input del filtro chiama questo metodo quando riceve una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="52c49-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="52c49-112">Questo metodo imposta il [**flag CBaseRenderer:: m \_ BEOS**](cbaserenderer-m-beos.md) su **true** e chiama il metodo [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) per pianificare un evento [**EC \_ complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="52c49-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="52c49-113">Se il filtro è sospeso e in attesa di un campione, questo metodo completa la transizione di stato.</span><span class="sxs-lookup"><span data-stu-id="52c49-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c49-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c49-114">Requirements</span></span>



| <span data-ttu-id="52c49-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c49-115">Requirement</span></span> | <span data-ttu-id="52c49-116">Valore</span><span class="sxs-lookup"><span data-stu-id="52c49-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c49-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52c49-117">Header</span></span><br/>  | <dl> <span data-ttu-id="52c49-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52c49-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="52c49-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="52c49-119">Library</span></span><br/> | <dl> <span data-ttu-id="52c49-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="52c49-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c49-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52c49-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c49-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="52c49-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




