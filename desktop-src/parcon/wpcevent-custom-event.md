---
description: Evento per utente che supporta fino a tre campi.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Evento WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227363"
---
# <a name="wpcevent_custom-event"></a>\_Evento personalizzato WPCEVENT

Evento per utente che supporta fino a tre campi.

Gli eventi vengono visualizzati nel **Visualizzatore attività** nell' **altra** sezione con la gerarchia seguente:

1.  Publisher

2.  Applicazione

3.  Evento


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Autore* 
</dt> <dd>

Server di pubblicazione dell'evento (ad esempio, un nome della società).

</dd> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione che genera l'evento.

</dd> <dt>

*Event* 
</dt> <dd>

Nome dell'evento.

</dd> <dt>

*Value1* 
</dt> <dd>

Campo personalizzato 1.

</dd> <dt>

*Value2* 
</dt> <dd>

Campo personalizzato 2.

</dd> <dt>

*Valore3* 
</dt> <dd>

Campo personalizzato 3.

</dd> <dt>

*Bloccato* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*Motivo* 
</dt> <dd>

Stringa personalizzata che fornisce informazioni aggiuntive sul motivo del blocco o non blocco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per i controlli padre](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**\_argomenti \_ CONVERSATIONINITEVENT di WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




