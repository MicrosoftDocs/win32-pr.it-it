---
description: Descrive la notifica passata alla funzione di \_ \_ richiamata della notifica del sink di visualizzazione della direttiva \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Struttura WFD_DISPLAY_SINK_NOTIFICATION (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311655"
---
# <a name="wfd_display_sink_notification-structure"></a>\_Struttura di \_ notifica del sink di visualizzazione della direttiva. \_

La struttura di **notifica del sink di visualizzazione della direttiva GMA \_ \_ \_** descrive la notifica passata alla funzione di [**callback di notifica del \_ \_ sink di \_ \_ visualizzazione**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Members

<dl> <dt>

**Intestazione**
</dt> <dd>

[**Intestazione dell' \_ \_ \_ oggetto \_ sink di visualizzazione della direttiva**](wfd-display-sink-object-header.md) , che descrive i dati inclusi nella notifica.

</dd> <dt>

**type**
</dt> <dd>

Un valore del tipo di notifica del sink di visualizzazione della direttiva, che indica il tipo di notifica. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md) Questo parametro determina inoltre le informazioni da utilizzare nell'Unione sottostante.

</dd> <dt>

**strRemoteDeviceName**
</dt> <dd>

Contiene una stringa a terminazione NULL che contiene il nome del dispositivo remoto. \_ \_ \_ \_ La lunghezza massima del nome dispositivo del sink di direttiva \_ viene definita come valore (32).

</dd> <dt>

**RemoteDeviceAddress**
</dt> <dd>

Un [**\_ \_ indirizzo Mac DOT11**](dot11-mac-address-type.md) che contiene il BSSID del dispositivo remoto.

</dd> <dt>

**ProvisioningRequestInfo**
</dt> <dd>

Informazioni su una richiesta di provisioning. Usare questa se il *tipo* ha il valore **ProvisioningRequestNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Handle della sessione.

</dd> <dt>

**PossibleConfigMethods**
</dt> <dd>

Metodi possibili per visualizzare l'interfaccia utente per l'accettazione interattiva.

</dd> </dl> </dd> <dt>

**ReconnectRequestInfo**
</dt> <dd>

Informazioni su una richiesta di riconnessione. Usare questa se il *tipo* ha il valore **ReconnectRequestNotification**.

<dl> <dt>

**GroupID**
</dt> <dd>

ID del gruppo.

</dd> </dl> </dd> <dt>

**ConnectedInfo**
</dt> <dd>

Informazioni su una notifica connessa. Usare questa se il *tipo* ha il valore **ConnectedNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Handle della sessione.

</dd> <dt>

**guidSessionInterface**
</dt> <dd>

GUID che indica l'interfaccia di sessione.

</dd> <dt>

**GroupID**
</dt> <dd>

ID del gruppo.

</dd> <dt>

**strProfile**
</dt> <dd>

Puntatore a una stringa con terminazione NULL che descrive il profilo.

</dd> <dt>

**LocalAddress**
</dt> <dd>

Indirizzo locale.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

Indirizzo remoto.

</dd> <dt>

**uRTSPPort**
</dt> <dd>

Porta RTSP.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




