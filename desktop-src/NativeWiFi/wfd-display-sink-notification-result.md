---
description: Descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di una notifica del sink di visualizzazione nella funzione \_ WFD DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink.h)
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
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780081"
---
# <a name="wfd_display_sink_notification_result-structure"></a>Struttura RISULTATO NOTIFICA SINK VISUALIZZAZIONE WFD \_ \_ \_ \_

La **struttura WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ RESULT** descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di una notifica del sink di visualizzazione nella [**funzione \_ WFD DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK.**](wfd-display-sink-notification-callback.md)

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

Intestazione [**dell'oggetto \_ SINK DISPLAY \_ \_ DI \_ WFD**](wfd-display-sink-object-header.md) che descrive i dati inclusi nel risultato della notifica.

</dd> <dt>

**type**
</dt> <dd>

Valore [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ TYPE**](wfd-display-sink-notification-type.md) che indica il tipo di risultato della notifica. Questo parametro determina anche le informazioni da usare nell'unione seguente.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Informazioni sul risultato di una richiesta di provisioning. Usare questo valore *se il tipo* ha il valore **ProvisioningRequestNotification**.

<dl> <dt>

**Metodo di configurazione**
</dt> <dd>

Metodo per visualizzare l'interfaccia utente per l'accettazione interattiva.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Numero di caratteri wide in *Passkey,* senza contare alcun carattere di terminazione NULL.

</dd> <dt>

**Passkey**
</dt> <dd>

Contiene la chiave di passaggio come matrice di caratteri wide. WFD \_ SINK \_ WPS INFO MAX PASSKEY LENGTH è definito come \_ valore \_ \_ \_ (8).

</dd> </dl> </dd> <dt>

**Riconnettere i dati**
</dt> <dd>

Informazioni sul risultato di una richiesta di riconnessione. Usare questo valore *se type* ha il valore **ReconnectRequestNotification**.

<dl> <dt>

**strProfile**
</dt> <dd>

Puntatore a una stringa con terminazione NULL che descrive il profilo.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




