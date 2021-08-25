---
description: Evento per utente che supporta fino a tre campi.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8082e03aa6dfea8cd2fd461feec093de71a1ada8051b8fb88295d0bbbf570b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951551"
---
# <a name="wpcevent_custom-event"></a>Evento WPCEVENT \_ CUSTOM

Evento per utente che supporta fino a tre campi.

Gli eventi vengono visualizzati nel **Visualizzatore attività** nella **sezione Altro** con la gerarchia seguente:

1.  Publisher

2.  Applicazione

3.  Event


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Autore* 
</dt> <dd>

Autore dell'evento , ad esempio il nome di una società.

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

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*Motivo* 
</dt> <dd>

Stringa personalizzata che fornisce informazioni aggiuntive sul motivo del blocco o meno.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per Controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




