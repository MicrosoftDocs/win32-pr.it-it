---
description: Il metodo OnDirectRender raccoglie informazioni sulla temporizzazione che controlla la sincronizzazione e il controllo della qualità.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Metodo CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326562"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="e47ec-103">CBaseVideoRenderer. OnDirectRender, metodo</span><span class="sxs-lookup"><span data-stu-id="e47ec-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="e47ec-104">Il metodo **OnDirectRender** raccoglie informazioni sulla temporizzazione che controlla la sincronizzazione e il controllo della qualità.</span><span class="sxs-lookup"><span data-stu-id="e47ec-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="e47ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e47ec-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="e47ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e47ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e47ec-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="e47ec-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e47ec-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e47ec-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e47ec-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e47ec-109">Return value</span></span>

<span data-ttu-id="e47ec-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e47ec-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e47ec-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e47ec-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e47ec-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e47ec-112">Remarks</span></span>

<span data-ttu-id="e47ec-113">Chiamare questo metodo anziché [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) e [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="e47ec-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="e47ec-114">Questo metodo viene utilizzato dal renderer video DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="e47ec-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e47ec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e47ec-115">Requirements</span></span>



| <span data-ttu-id="e47ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e47ec-116">Requirement</span></span> | <span data-ttu-id="e47ec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e47ec-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e47ec-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e47ec-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e47ec-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e47ec-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e47ec-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e47ec-120">Library</span></span><br/> | <dl> <span data-ttu-id="e47ec-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e47ec-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e47ec-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e47ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e47ec-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e47ec-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




