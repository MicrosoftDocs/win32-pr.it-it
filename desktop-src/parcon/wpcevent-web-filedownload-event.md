---
description: Evento per utente generato durante il tentativo di scaricare file dal Web. Questo evento viene generato dalle applicazioni richieste da Controllo genitori.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7430b87e7c227fe351e3182f344c60ece0b5a3138b94fe19fee950f96ec24b6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112711"
---
# <a name="wpcevent_web_filedownload-event"></a>Evento WPCEVENT \_ WEB \_ FILEDOWNLOAD

Evento per utente generato durante il tentativo di scaricare file dal Web. Questo evento viene generato dalle applicazioni richieste da Controllo genitori.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* 
</dt> <dd>

Origine URL che sta tentando di scaricare.

</dd> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione che genera l'evento.

</dd> <dt>

*Version* 
</dt> <dd>

Versione dell'applicazione che genera l'evento.

</dd> <dt>

*Bloccato* 
</dt> <dd>

Valore [**dell'enumerazione \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso di destinazione del file.

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

 

 




