---
title: WMT_STATUS di eventi in DirectShow
description: Notifica \_ dell'evento WMT STATUS in DirectShow
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media Format SDK, WMT_STATUS notifiche degli eventi in DirectShow
- Windows Media Format SDK, notifiche degli eventi
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), WMT_STATUS di eventi in DirectShow
- ASF (Advanced Systems Format), WMT_STATUS notifiche degli eventi in DirectShow
- Advanced Systems Format (ASF), notifiche degli eventi
- ASF (Advanced Systems Format), notifiche degli eventi
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,notifiche degli eventi
- DirectShow,WMT_STATUS eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4bbe430f16872baf94a0d47417381bc8bcd23d5c9fbbdb69ff2496cd873908
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089631"
---
# <a name="wmt_status-event-notification-in-directshow"></a>Notifica \_ dell'evento WMT STATUS in DirectShow

Sia il lettore ASF che il writer ASF inoltrano [**gli eventi WMT \_ STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) alle applicazioni. Il writer inoltra tutti questi eventi e il lettore inoltra solo quelli relativi all'acquisizione della licenza DRM. Per ricevere queste notifiche degli eventi nell'applicazione, aggiungere un caso per **EC \_ WMT \_ EVENT** nella funzione di gestione degli eventi. Il *parametro lParam1* associato all'evento contiene il codice **WMT \_ STATUS** (che può essere **WMT \_ ERROR)** e lParam2 contiene un ELEMENTO [**\_ WMT EVENT \_ \_ DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) am che include **HRESULT**.

 

 