---
description: Il renderer video è stato eliminato o rimosso dal grafico.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325496"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="ec558-103">\_finestra EC \_ distrutta</span><span class="sxs-lookup"><span data-stu-id="ec558-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="ec558-104">Il renderer video è stato eliminato o rimosso dal grafico.</span><span class="sxs-lookup"><span data-stu-id="ec558-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec558-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec558-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec558-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ec558-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ec558-107">(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer video.</span><span class="sxs-lookup"><span data-stu-id="ec558-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ec558-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ec558-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ec558-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="ec558-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ec558-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="ec558-110">Default Action</span></span>

<span data-ttu-id="ec558-111">Il gestore del grafico del filtro rilascia questa finestra come stato attivo, tramite l'interfaccia [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="ec558-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="ec558-112">Non invia la notifica degli eventi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec558-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec558-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec558-113">Remarks</span></span>

<span data-ttu-id="ec558-114">Il renderer video Invia questo evento quando lascia il grafico del filtro, nel metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="ec558-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="ec558-115">Inviando l'evento quando il filtro viene eliminato definitivamente potrebbe essere troppo tardi, perché a questo punto è possibile che anche il gestore del grafo del filtro venga eliminato.</span><span class="sxs-lookup"><span data-stu-id="ec558-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="ec558-116">Questo evento consente ad altri filtri di acquisire risorse che dipendono dallo stato attivo della finestra, ad esempio i dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="ec558-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec558-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec558-117">Requirements</span></span>



| <span data-ttu-id="ec558-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec558-118">Requirement</span></span> | <span data-ttu-id="ec558-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ec558-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec558-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec558-120">Header</span></span><br/> | <dl> <span data-ttu-id="ec558-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec558-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec558-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec558-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec558-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="ec558-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ec558-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ec558-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




