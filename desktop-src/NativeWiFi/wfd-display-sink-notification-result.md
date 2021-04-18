---
description: Descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di un sink di visualizzazione notifica \_ nella \_ \_ funzione di richiamata della notifica del sink di visualizzazione della direttiva \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Struttura WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318263"
---
# <a name="wfd_display_sink_notification_result-structure"></a>\_Struttura del \_ risultato della notifica del sink di visualizzazione della \_ direttiva. \_

La struttura del risultato della notifica del sink di visualizzazione della direttiva per la visualizzazione del sink descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di un sink di visualizzazione notifica nella funzione di [**\_ \_ \_ \_ richiamata della notifica di sink**](wfd-display-sink-notification-callback.md) **\_ \_ \_ \_**

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Members

<dl> <dt>

**Intestazione**
</dt> <dd>

[**Intestazione dell' \_ \_ \_ oggetto \_ sink di visualizzazione della direttiva**](wfd-display-sink-object-header.md) , che descrive i dati inclusi nel risultato della notifica.

</dd> <dt>

**type**
</dt> <dd>

Un valore del tipo di notifica del sink di visualizzazione della direttiva, che indica il tipo di risultato della notifica. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md) Questo parametro determina inoltre le informazioni da utilizzare nell'Unione sottostante.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Informazioni sul risultato di una richiesta di provisioning. Usare questa se il *tipo* ha il valore **ProvisioningRequestNotification**.

<dl> <dt>

**ConfigMethod**
</dt> <dd>

Metodo per visualizzare l'interfaccia utente per l'accettazione interattiva.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Il numero di caratteri wide nella *passkey*, senza contare alcun carattere di terminazione null.

</dd> <dt>

**Passkey**
</dt> <dd>

Contiene il tasto pass come matrice di caratteri wide. \_ \_ \_ \_ \_ La lunghezza di passkey massima delle informazioni WPS del sink \_ di direttiva è definita come valore (8).

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Informazioni sul risultato di una richiesta di riconnessione. Usare questa se il *tipo* ha il valore **ReconnectRequestNotification**.

<dl> <dt>

**strProfile**
</dt> <dd>

Puntatore a una stringa con terminazione NULL che descrive il profilo.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




