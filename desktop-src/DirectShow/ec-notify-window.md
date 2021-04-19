---
description: Invia una notifica a un filtro della finestra del renderer video.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332195"
---
# <a name="ec_notify_window"></a><span data-ttu-id="9d65a-103">\_finestra notifica \_ EC</span><span class="sxs-lookup"><span data-stu-id="9d65a-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="9d65a-104">Invia una notifica a un filtro della finestra del renderer video.</span><span class="sxs-lookup"><span data-stu-id="9d65a-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d65a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d65a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d65a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9d65a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9d65a-107">(**HWND**) Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="9d65a-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="9d65a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9d65a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9d65a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="9d65a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9d65a-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="9d65a-110">Default Action</span></span>

<span data-ttu-id="9d65a-111">Questo evento viene utilizzato internamente da DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9d65a-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="9d65a-112">Il gestore del grafico del filtro non passa questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d65a-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="9d65a-113">Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.</span><span class="sxs-lookup"><span data-stu-id="9d65a-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d65a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d65a-114">Remarks</span></span>

<span data-ttu-id="9d65a-115">Quando un renderer video è connesso, verifica se il pin di output upstream supporta l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="9d65a-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="9d65a-116">In tal caso, il renderer Invia questo evento al filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="9d65a-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d65a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d65a-117">Requirements</span></span>



| <span data-ttu-id="9d65a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d65a-118">Requirement</span></span> | <span data-ttu-id="9d65a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9d65a-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d65a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d65a-120">Header</span></span><br/> | <dl> <span data-ttu-id="9d65a-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d65a-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d65a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d65a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d65a-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="9d65a-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9d65a-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9d65a-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




