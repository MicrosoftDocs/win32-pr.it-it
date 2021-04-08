---
description: Evento per utente generato dal sistema durante il tentativo di avviare una partita. I diversi valori dei campi sono forniti dal sistema di Esplora giochi e dai metadati del file di definizione del gioco (GDF) corrispondenti forniti dai giochi supportati.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: Evento WPCEVENT_GAME_START (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049973"
---
# <a name="wpcevent_game_start-event"></a>Evento di avvio del \_ gioco WPCEVENT \_

Evento per utente generato dal sistema durante il tentativo di avviare una partita. I diversi valori dei campi sono forniti dal sistema di Esplora giochi e dai metadati del file di definizione del gioco (GDF) corrispondenti forniti dai giochi supportati.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppID* 
</dt> <dd>

GUID del gioco che ha tentato di avviarsi.

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

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*DescCount* 
</dt> <dd>

Numero di descrittori presenti nel campo del descrittore.

</dd> <dt>

*Descrittore* 
</dt> <dd>

Stringa delimitata che contiene i descrittori bloccati per il gioco.

</dd> <dt>

*PID* 
</dt> <dd>

ID processo del gioco, utilizzato per la correlazione con un arresto dello shim del processo.

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

 

 




