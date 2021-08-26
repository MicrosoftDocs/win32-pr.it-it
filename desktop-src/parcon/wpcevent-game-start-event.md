---
description: Evento per utente generato dal sistema durante il tentativo di avviare un gioco. Vari valori di campo vengono forniti dal sistema Games Explorer e dai metadati GDF (Game Definition File) corrispondenti forniti dai giochi supportati.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41367a47a9bace8dd615ab4b6eea0a875099aab465c285389478c4bee0a39392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951501"
---
# <a name="wpcevent_game_start-event"></a>Evento WPCEVENT \_ GAME \_ START

Evento per utente generato dal sistema durante il tentativo di avviare un gioco. Vari valori di campo vengono forniti dal sistema Games Explorer e dai metadati GDF (Game Definition File) corrispondenti forniti dai giochi supportati.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppID* 
</dt> <dd>

GUID del gioco che ha tentato di avviare.

</dd> <dt>

*InstanceID* 
</dt> <dd>

GUID utilizzato per distinguere tra più installazioni.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Stringa di versione per il gioco.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso della directory primaria dell'installazione del gioco.

</dd> <dt>

*Rating* 
</dt> <dd>

Stringa che identifica il livello di classificazione di un gioco all'interno del sistema di classificazione.

</dd> <dt>

*RatingSystem* 
</dt> <dd>

GUID che identifica il sistema di classificazione corrente a cui si applica il livello di classificazione.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*DescCount* 
</dt> <dd>

Numero di descrittori presenti nel campo del descrittore.

</dd> <dt>

*Descrittore* 
</dt> <dd>

Stringa delimitata che contiene i descrittori bloccati per il gioco.

</dd> <dt>

*Pid* 
</dt> <dd>

ID processo del gioco, usato per correlare con un arresto shim del processo.

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

 

 




