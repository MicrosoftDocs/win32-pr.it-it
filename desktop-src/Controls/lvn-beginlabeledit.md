---
title: LVN_BEGINLABELEDIT di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco l'inizio della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5b5ecfed8fdc15ec2779e204d01b0375c7da702e2a2e9fe8a3cdc3b178b0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830652"
---
# <a name="lvn_beginlabeledit-notification-code"></a>Codice di notifica LVN \_ BEGINLABELEDIT

Notifica alla finestra padre di un controllo visualizzazione elenco l'inizio della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Il **membro** dell'elemento di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui **membro iItem** identifica l'elemento da modificare. Si noti che gli elementi secondari non possono essere modificati. Il **membro iSubItem** è sempre impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire all'utente di modificare l'etichetta, restituire **FALSE.**

Per impedire all'utente di modificare l'etichetta, restituire **TRUE.**

## <a name="remarks"></a>Commenti

Quando inizia la modifica delle etichette, viene creato, posizionato e inizializzato un controllo di modifica. Prima che venga visualizzato, il controllo visualizzazione elenco invia alla finestra padre un codice di notifica LVN \_ BEGINLABELEDIT.

Per personalizzare la modifica delle etichette, implementare un gestore per LVN BEGINLABELEDIT e fare in modo che invii un messaggio \_ [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al controllo di visualizzazione elenco. Se un'etichetta viene modificata, il valore restituito sarà un handle per il controllo di modifica. Usare questo handle per personalizzare il controllo di modifica inviando i normali **messaggi EM \_ XXX.**

Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di notifica [LVN \_ ENDLABELEDIT.](lvn-endlabeledit.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





