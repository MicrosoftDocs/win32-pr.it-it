---
description: È stato eseguito il rendering di tutti i dati di un flusso specifico.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328459"
---
# <a name="ec_complete"></a><span data-ttu-id="9bd42-103">EC \_ completato</span><span class="sxs-lookup"><span data-stu-id="9bd42-103">EC\_COMPLETE</span></span>

<span data-ttu-id="9bd42-104">È stato eseguito il rendering di tutti i dati di un flusso specifico.</span><span class="sxs-lookup"><span data-stu-id="9bd42-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bd42-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bd42-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd42-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9bd42-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9bd42-107">(**HRESULT**) Stato del flusso al termine dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9bd42-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="9bd42-108">Se non si sono verificati errori durante la riproduzione, il valore è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9bd42-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="9bd42-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9bd42-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9bd42-110">(**IUnknown** \* ) Zero o un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer.</span><span class="sxs-lookup"><span data-stu-id="9bd42-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9bd42-111">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="9bd42-111">Default Action</span></span>

<span data-ttu-id="9bd42-112">Per impostazione predefinita, il gestore del grafico del filtro non trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bd42-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="9bd42-113">Tuttavia, dopo il **\_ completamento** di tutti i flussi nel report grafico EC, il gestore del grafico del filtro pubblica un evento di **\_ completamento EC** separato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bd42-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="9bd42-114">Se l'azione predefinita è disabilitata per questo evento, l'applicazione riceve tutti gli **eventi \_ completi EC** dai renderer.</span><span class="sxs-lookup"><span data-stu-id="9bd42-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bd42-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bd42-115">Remarks</span></span>

<span data-ttu-id="9bd42-116">Un filtro renderer Invia questo evento quando riceve una notifica di fine flusso.</span><span class="sxs-lookup"><span data-stu-id="9bd42-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="9bd42-117">(La fine del flusso viene segnalata tramite il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ). Il filtro Invia esattamente un evento **EC \_ complete** per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="9bd42-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="9bd42-118">Il filtro deve elaborare tutti gli esempi in sospeso prima di inviare l'evento.</span><span class="sxs-lookup"><span data-stu-id="9bd42-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="9bd42-119">L'arresto di un renderer Reimposta lo stato della fine del flusso memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="9bd42-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="9bd42-120">Se il renderer è sospeso, non invia la funzione **EC \_ completa** fino a quando non viene chiamato il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="9bd42-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="9bd42-121">Continua inoltre a inviare eventi **EC \_ completi** per ogni transizione dalla pausa per l'esecuzione, fino a quando il filtro non viene interrotto o scaricato.</span><span class="sxs-lookup"><span data-stu-id="9bd42-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="9bd42-122">I filtri impostano il parametro *lParam2* su un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="9bd42-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="9bd42-123">Se l'azione predefinita è abilitata, il gestore del grafico del filtro imposta questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="9bd42-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd42-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bd42-124">Requirements</span></span>



| <span data-ttu-id="9bd42-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd42-125">Requirement</span></span> | <span data-ttu-id="9bd42-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9bd42-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd42-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bd42-127">Header</span></span><br/> | <dl> <span data-ttu-id="9bd42-128"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bd42-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd42-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bd42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd42-130">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="9bd42-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9bd42-131">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9bd42-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="9bd42-132">Renderer video alternativi</span><span class="sxs-lookup"><span data-stu-id="9bd42-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




