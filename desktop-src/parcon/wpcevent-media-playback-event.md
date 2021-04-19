---
description: Evento per utente generato da un tentativo di riprodurre contenuto con un'applicazione multimediale connessa ai controlli padre.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: Evento WPCEVENT_MEDIA_PLAYBACK (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320728"
---
# <a name="wpcevent_media_playback-event"></a>\_Evento di \_ riproduzione multimediale WPCEVENT

Evento per utente generato da un tentativo di riprodurre contenuto con un'applicazione multimediale connessa ai controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione multimediale che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione multimediale che genera l'evento.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di supporto WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) che indica le informazioni sul tipo di file multimediale a cui si accede.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso dell'origine del contenuto multimediale.

</dd> <dt>

*Title* 
</dt> <dd>

Metadati del titolo per il contenuto.

</dd> <dt>

*PML* 
</dt> <dd>

Livello di gestione padre.

</dd> <dt>

*Album* 
</dt> <dd>

Metadati dell'album per il contenuto.

</dd> <dt>

*Esplicita* 
</dt> <dd>

Valore dell'enumerazione [**\_ \_ esplicita del supporto WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) che indica le informazioni sulla classificazione esplicita del file multimediale.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

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

 

 




