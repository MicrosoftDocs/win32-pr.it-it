---
description: Evento per utente generato da un'applicazione di messaggistica istantanea quando un'entità tenta di partecipare a una conversazione in corso in Controllo genitori.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 181bc849cf89e8a78a7a5aaad97463baf0c611d99ca0dc05caf9bfaf879eb804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951291"
---
# <a name="wpcevent_im_join-event"></a>Evento WPCEVENT \_ IM \_ JOIN

Evento per utente generato da un'applicazione di messaggistica istantanea quando un'entità tenta di partecipare a una conversazione in corso in Controllo genitori.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

Stringa di identità dell'account di messaggistica istantanea per questo utente.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificatore per questa conversazione.

</dd> <dt>

*JoiningIP* 
</dt> <dd>

Stringa contenente l'indirizzo IP del computer che sta partecipando alla conversazione.

</dd> <dt>

*JoinUser* 
</dt> <dd>

Stringa di identità dell'account di messaggistica istantanea per l'utente che si sta unendo.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Numero di partecipanti presenti nella conversazione e con identità definite nel campo del membro.

</dd> <dt>

*Membro* 
</dt> <dd>

Stringa delimitata che contiene stringhe di identità dell'account di messaggistica istantanea per tutti i membri correnti di questa conversazione.

</dd> <dt>

*Mittente* 
</dt> <dd>

Stringa di identità dell'account di messaggistica istantanea per l'utente che effettua la richiesta di partecipazione alla conversazione.

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

 

 




