---
description: Evento per utente generato durante il tentativo di scaricare i file dal Web. Questo evento viene generato dalle applicazioni richieste dai controlli padre.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: Evento WPCEVENT_WEB_FILEDOWNLOAD (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318390"
---
# <a name="wpcevent_web_filedownload-event"></a>Evento di DOWNLOAD del fileWPCEVENT \_ Web \_

Evento per utente generato durante il tentativo di scaricare i file dal Web. Questo evento viene generato dalle applicazioni richieste dai controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* 
</dt> <dd>

Origine dell'URL che tenta di scaricare.

</dd> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione che genera l'evento.

</dd> <dt>

*Versione* 
</dt> <dd>

Versione dell'applicazione che genera l'evento.

</dd> <dt>

*Bloccato* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso di destinazione del file.

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

 

 




