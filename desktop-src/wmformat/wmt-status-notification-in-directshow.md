---
title: WMT_STATUS la notifica degli eventi in DirectShow
description: '\_Notifica degli eventi dello stato WMT in DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media Format SDK, WMT_STATUS notifiche degli eventi in DirectShow
- Windows Media Format SDK, notifiche degli eventi
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), WMT_STATUS notifiche degli eventi in DirectShow
- ASF (Advanced Systems Format), WMT_STATUS notifiche degli eventi in DirectShow
- ASF (Advanced Systems Format), notifiche degli eventi
- ASF (formato avanzato dei sistemi), notifiche degli eventi
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, notifiche degli eventi
- DirectShow, WMT_STATUS notifiche degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223941"
---
# <a name="wmt_status-event-notification-in-directshow"></a><span data-ttu-id="dbc08-114">\_Notifica degli eventi dello stato WMT in DirectShow</span><span class="sxs-lookup"><span data-stu-id="dbc08-114">WMT\_STATUS Event Notification in DirectShow</span></span>

<span data-ttu-id="dbc08-115">Sia il Reader ASF che il writer ASF inviano eventi di [**\_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dbc08-115">Both the ASF Reader and the ASF Writer forward [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) events to applications.</span></span> <span data-ttu-id="dbc08-116">Il writer trasmette tutti questi eventi e il lettore trasmette solo quelli che riguardano l'acquisizione di licenze DRM.</span><span class="sxs-lookup"><span data-stu-id="dbc08-116">The writer forwards all such events, and the reader forwards only those that pertain to DRM license acquisition.</span></span> <span data-ttu-id="dbc08-117">Per ricevere le notifiche degli eventi nell'applicazione, aggiungere un case per l' **\_ \_ evento EC WMT** nella funzione di gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="dbc08-117">To receive these event notifications in your application, add a case for the **EC\_WMT\_EVENT** in your event-handling function.</span></span> <span data-ttu-id="dbc08-118">Il parametro *lParam1* associato all'evento contiene il codice **di \_ stato WMT** (che può essere **WMT \_ Error**) e lParam2 contiene i [**\_ dati dell' \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) che includono **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dbc08-118">The *lParam1* parameter associated with the event contains the **WMT\_STATUS** code (which can be **WMT\_ERROR**) and lParam2 contains an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) that includes the **HRESULT**.</span></span>

 

 