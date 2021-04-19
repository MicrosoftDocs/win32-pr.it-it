---
description: Il metodo Notify riceve una notifica di richiesta di modifica della qualità.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Metodo CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326564"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="11874-103">Metodo CBaseVideoRenderer. Notify</span><span class="sxs-lookup"><span data-stu-id="11874-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="11874-104">Il `Notify` metodo riceve una notifica che viene richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="11874-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="11874-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11874-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="11874-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11874-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11874-107">*pSelf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11874-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11874-108">Puntatore al filtro che invia la notifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="11874-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="11874-109">*domande* e risposte \[\]</span><span class="sxs-lookup"><span data-stu-id="11874-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11874-110">Struttura delle notifiche di qualità.</span><span class="sxs-lookup"><span data-stu-id="11874-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11874-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11874-111">Return value</span></span>

<span data-ttu-id="11874-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11874-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11874-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="11874-113">Remarks</span></span>

<span data-ttu-id="11874-114">Questa funzione membro implementa il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) nel renderer video.</span><span class="sxs-lookup"><span data-stu-id="11874-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="11874-115">Questo metodo viene chiamato, in genere da Filter Graph Manager, quando è necessario tagliare la qualità.</span><span class="sxs-lookup"><span data-stu-id="11874-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="11874-116">Questo problema può verificarsi quando la qualità della riproduzione audio è stata aumentata fino a quando la qualità della riproduzione video deve essere ridotta.</span><span class="sxs-lookup"><span data-stu-id="11874-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="11874-117">`Notify` imposta il membro dati **\_ trThrottle m** su un valore delay da inserire tra i frame da [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="11874-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11874-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11874-118">Requirements</span></span>



| <span data-ttu-id="11874-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="11874-119">Requirement</span></span> | <span data-ttu-id="11874-120">Valore</span><span class="sxs-lookup"><span data-stu-id="11874-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11874-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11874-121">Header</span></span><br/>  | <dl> <span data-ttu-id="11874-122"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11874-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11874-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="11874-123">Library</span></span><br/> | <dl> <span data-ttu-id="11874-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11874-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11874-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11874-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11874-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="11874-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




