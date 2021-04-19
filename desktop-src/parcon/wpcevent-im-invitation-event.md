---
description: Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica immediata.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Evento WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316430"
---
# <a name="wpcevent_im_invitation-event"></a>\_ \_ Evento invito WPCEVENT im

Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica immediata.


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

Stringa di identità dell'account di messaggistica immediata.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificatore per la conversazione.

</dd> <dt>

*RequestingIP* 
</dt> <dd>

Stringa contenente l'indirizzo IP del computer che invia l'invito.

</dd> <dt>

*Mittente* 
</dt> <dd>

Stringa di identità dell'account di messaggistica immediata per l'account che ha emesso l'invito.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero di destinatari che ricevono l'invito e che hanno identità definite nel campo del destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Stringa delimitata che contiene le stringhe di identità dell'account di messaggistica immediata per i destinatari dell'invito.

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

 

 




