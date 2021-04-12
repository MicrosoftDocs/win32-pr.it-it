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
# <a name="wmt_status-event-notification-in-directshow"></a>\_Notifica degli eventi dello stato WMT in DirectShow

Sia il Reader ASF che il writer ASF inviano eventi di [**\_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) alle applicazioni. Il writer trasmette tutti questi eventi e il lettore trasmette solo quelli che riguardano l'acquisizione di licenze DRM. Per ricevere le notifiche degli eventi nell'applicazione, aggiungere un case per l' **\_ \_ evento EC WMT** nella funzione di gestione degli eventi. Il parametro *lParam1* associato all'evento contiene il codice **di \_ stato WMT** (che può essere **WMT \_ Error**) e lParam2 contiene i [**\_ dati dell' \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) che includono **HRESULT**.

 

 