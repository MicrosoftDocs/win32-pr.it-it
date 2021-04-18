---
description: Un renderer video richiede un oggetto Repaint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324157"
---
# <a name="ec_repaint"></a><span data-ttu-id="56dc8-103">ridisegno EC \_</span><span class="sxs-lookup"><span data-stu-id="56dc8-103">EC\_REPAINT</span></span>

<span data-ttu-id="56dc8-104">Un renderer video richiede un oggetto Repaint.</span><span class="sxs-lookup"><span data-stu-id="56dc8-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="56dc8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="56dc8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dc8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="56dc8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="56dc8-107">(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input del renderer video o **null**.</span><span class="sxs-lookup"><span data-stu-id="56dc8-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="56dc8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="56dc8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="56dc8-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="56dc8-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="56dc8-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="56dc8-110">Default Action</span></span>

<span data-ttu-id="56dc8-111">Il parametro *lParam1* potrebbe specificare il pin di input del renderer video.</span><span class="sxs-lookup"><span data-stu-id="56dc8-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="56dc8-112">In tal caso, il gestore del grafico del filtro trova il pin di output connesso al pin e lo interroga per l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="56dc8-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="56dc8-113">Se il pin di output supporta **IMediaEventSink**, il gestore del grafo dei filtri chiama [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) con il \_ codice dell'evento EC Repaint.</span><span class="sxs-lookup"><span data-stu-id="56dc8-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="56dc8-114">Ciò consente al filtro upstream di inviare nuovamente l'ultimo esempio.</span><span class="sxs-lookup"><span data-stu-id="56dc8-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="56dc8-115">Se *lParam1* è **null** o se il PIN non supporta [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)o se il metodo [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) ha esito negativo, il gestore del grafico del filtro gestisce l' \_ evento di ridisegno EC da solo.</span><span class="sxs-lookup"><span data-stu-id="56dc8-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="56dc8-116">Il relativo comportamento dipende dallo stato del grafo:</span><span class="sxs-lookup"><span data-stu-id="56dc8-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="56dc8-117">Running: ignora l'evento.</span><span class="sxs-lookup"><span data-stu-id="56dc8-117">Running: Ignores the event.</span></span> <span data-ttu-id="56dc8-118">Il renderer riceverà l'esempio successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="56dc8-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="56dc8-119">Paused: Cerca il grafico nella posizione corrente, scaricando quindi il filtro e riaccodando i dati.</span><span class="sxs-lookup"><span data-stu-id="56dc8-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="56dc8-120">Arrestato: sospende e arresta il grafico, riaccodando quindi i dati.</span><span class="sxs-lookup"><span data-stu-id="56dc8-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="56dc8-121">Per impostazione predefinita, il gestore del grafico del filtro non passa questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56dc8-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="56dc8-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="56dc8-122">Remarks</span></span>

<span data-ttu-id="56dc8-123">I renderer video inviano questo messaggio quando ricevono un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) e non contengono dati da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="56dc8-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="56dc8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56dc8-124">Requirements</span></span>



| <span data-ttu-id="56dc8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dc8-125">Requirement</span></span> | <span data-ttu-id="56dc8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="56dc8-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56dc8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56dc8-127">Header</span></span><br/> | <dl> <span data-ttu-id="56dc8-128"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="56dc8-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dc8-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56dc8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dc8-130">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="56dc8-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="56dc8-131">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="56dc8-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

