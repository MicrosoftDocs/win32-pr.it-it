---
description: Il metodo SendQuality Invia un messaggio di qualità per indicare cosa deve fare il fornitore per la qualità.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Metodo CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325349"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="3cf59-103">CBaseVideoRenderer. SendQuality, metodo</span><span class="sxs-lookup"><span data-stu-id="3cf59-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="3cf59-104">Il `SendQuality` metodo invia un messaggio di qualità per indicare cosa deve fare il fornitore per la qualità.</span><span class="sxs-lookup"><span data-stu-id="3cf59-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf59-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cf59-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="3cf59-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cf59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf59-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="3cf59-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf59-108">Quantità di tempo in cui il frame è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="3cf59-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="3cf59-109">*trRealStream*</span><span class="sxs-lookup"><span data-stu-id="3cf59-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf59-110">Currentstream tempo.</span><span class="sxs-lookup"><span data-stu-id="3cf59-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf59-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cf59-111">Return value</span></span>

<span data-ttu-id="3cf59-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3cf59-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf59-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cf59-113">Remarks</span></span>

<span data-ttu-id="3cf59-114">Questa funzione membro invia un messaggio di controllo di qualità upstream per controllare la gestione della qualità.</span><span class="sxs-lookup"><span data-stu-id="3cf59-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="3cf59-115">La natura del messaggio di qualità, ovvero se ridurre o aumentare il numero di campioni, viene determinata nell'implementazione della gestione della qualità in questa classe derivata (vedere [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="3cf59-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf59-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cf59-116">Requirements</span></span>



| <span data-ttu-id="3cf59-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf59-117">Requirement</span></span> | <span data-ttu-id="3cf59-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3cf59-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf59-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3cf59-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3cf59-120"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cf59-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cf59-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3cf59-121">Library</span></span><br/> | <dl> <span data-ttu-id="3cf59-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cf59-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf59-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cf59-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf59-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="3cf59-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




