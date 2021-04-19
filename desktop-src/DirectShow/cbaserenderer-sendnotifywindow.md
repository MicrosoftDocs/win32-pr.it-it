---
description: Il metodo SendNotifyWindow invia una notifica al filtro upstream dell'handle della finestra video.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Metodo CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326427"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="eb07a-103">CBaseRenderer. SendNotifyWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="eb07a-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="eb07a-104">Il `SendNotifyWindow` metodo invia una notifica al filtro upstream dell'handle della finestra video.</span><span class="sxs-lookup"><span data-stu-id="eb07a-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb07a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb07a-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="eb07a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb07a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb07a-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="eb07a-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="eb07a-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output del filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="eb07a-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="eb07a-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="eb07a-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="eb07a-110">Handle per la finestra video o **null**.</span><span class="sxs-lookup"><span data-stu-id="eb07a-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb07a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb07a-111">Return value</span></span>

<span data-ttu-id="eb07a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="eb07a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb07a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb07a-113">Remarks</span></span>

<span data-ttu-id="eb07a-114">Se il pin di output del filtro upstream supporta l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , questo metodo invia il codice evento [**della \_ \_ finestra di notifica EC**](ec-notify-window.md) insieme all'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb07a-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="eb07a-115">I renderer video possono eseguire l'override dei metodi [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) per chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="eb07a-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="eb07a-116">Fornisce un meccanismo per informare il filtro upstream dell'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb07a-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="eb07a-117">In tal caso, eseguire l'override anche del metodo [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) e chiamare `SendNotifyWindow` con un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="eb07a-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb07a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb07a-118">Requirements</span></span>



| <span data-ttu-id="eb07a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb07a-119">Requirement</span></span> | <span data-ttu-id="eb07a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="eb07a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb07a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb07a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb07a-122"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb07a-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb07a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb07a-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb07a-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eb07a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb07a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb07a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb07a-126">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="eb07a-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




