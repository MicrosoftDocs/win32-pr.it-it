---
description: Definisce la funzione di callback&\# 8212, implementata nell'app&\# 8212; specificata per la funzione WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: Funzione di callback WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK (Wfdsink. h)
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
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311656"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Visualizzazione della funzione di callback di callback di \_ \_ \_ notifica sink \_

La funzione di **\_ \_ \_ \_ richiamata della notifica di sink di visualizzazione della direttiva GMA** definisce la funzione di callback, che viene implementata nell'app, specificata per la funzione [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .

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

*pNotification* \[ in\]
</dt> <dd>

Puntatore a uno struct che contiene i dati sulla notifica del sink di visualizzazione.

</dd> <dt>

*pNotificationResult* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a uno struct che contiene i dati che l'app può impostare facoltativamente per indicare il risultato dell'elaborazione della notifica del sink di visualizzazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




