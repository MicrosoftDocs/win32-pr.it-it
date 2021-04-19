---
description: Definisce il tipo di notifica passato alla \_ \_ funzione di \_ richiamata della notifica del sink di visualizzazione della direttiva \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Enumerazione WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311654"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a>\_Enumerazione del \_ tipo di notifica del sink di visualizzazione della \_ direttiva. \_

Il tipo enumerato del tipo di notifica del sink di visualizzazione della direttiva. definisce il tipo di notifica passato alla funzione di [**\_ \_ \_ \_ richiamata della notifica del sink di visualizzazione della direttiva**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**
</dt> <dd>

La notifica è una richiesta di provisioning.

</dd> <dt>

<span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**
</dt> <dd>

La notifica è una richiesta di riconnessione.

</dd> <dt>

<span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**
</dt> <dd>

La notifica è una notifica connessa.

</dd> <dt>

<span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**
</dt> <dd>

La notifica è una notifica disconnessa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




