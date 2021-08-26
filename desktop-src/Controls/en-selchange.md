---
title: EN_SELCHANGE di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a2398abd5058f57eeef6ad73f559a723e7df29315d38dfc9794a707740c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047421"
---
# <a name="en_selchange-notification-code"></a>Codice di notifica EN \_ SELCHANGE

Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) che riceve informazioni sulla selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce un valore.

## <a name="remarks"></a>Commenti

Per ricevere i \_ codici di notifica EN SELCHANGE, specificare [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

Questo codice di notifica viene inviato quando la posizione del cursore cambia e non viene selezionato alcun testo (la selezione è vuota). La posizione del cursore può cambiare quando l'utente fa clic con il mouse, si preme o si preme un tasto di direzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Selchange**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





