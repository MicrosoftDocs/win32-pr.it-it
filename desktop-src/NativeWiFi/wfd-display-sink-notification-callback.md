---
description: Definisce la funzione di callback&\# 8212; implementata nell'app&8212; specificata per la funzione \# WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK di callback (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: 7066f45b714c28b53747d0d0f1851bd94ac2ac902e5b4adba1d0746e8328b3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619976"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Funzione di \_ callback WFD DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK

La **funzione \_ WFD DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK** definisce la funzione di callback, implementata nell'app, specificata per la [**funzione WFDStartDisplaySink.**](wfdstartdisplaysink.md)

## <a name="syntax"></a>Sintassi


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore di contesto facoltativo passato alla funzione di callback.

</dd> <dt>

*pNotification* \[ Pollici\]
</dt> <dd>

Puntatore a uno struct contenente i dati relativi alla notifica del sink di visualizzazione.

</dd> <dt>

*pNotificationResult* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a uno struct contenente dati che l'app può facoltativamente impostare per indicare il risultato dell'elaborazione della notifica del sink di visualizzazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




