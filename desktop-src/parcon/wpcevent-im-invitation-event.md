---
description: Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica istantanea.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f29b1adc556e29e03f7c8a189567b98055187f80d1574e201c54e3af0c1c0aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951391"
---
# <a name="wpcevent_im_invitation-event"></a>Evento WPCEVENT \_ IM \_ INVITATION

Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica istantanea.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Stringa di versione per l'applicazione che genera l'evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Stringa di identità dell'account di messaggistica istantanea.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificatore della conversazione.

</dd> <dt>

*RequestingIP* 
</dt> <dd>

Stringa contenente l'indirizzo IP del computer che invia l'invito.

</dd> <dt>

*Mittente* 
</dt> <dd>

Stringa di identità dell'account di messaggistica istantanea per l'account che emette l'invito.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero di destinatari che ricevono l'invito e che dispongono di identità definite nel campo destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Stringa delimitata che contiene le stringhe di identità dell'account di messaggistica istantanea per i destinatari dell'invito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per il controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




