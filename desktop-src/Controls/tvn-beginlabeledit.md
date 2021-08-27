---
title: TVN_BEGINLABELEDIT di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero l'inizio della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8fdd2b75ee9f3dcc46e5449c275eeea141162f3d31f524b64e114a623bd915e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060091"
---
# <a name="tvn_beginlabeledit-notification-code"></a>Codice di notifica \_ TVN BEGINLABELEDIT

Notifica alla finestra padre di un controllo visualizzazione albero l'inizio della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Il **membro** dell'elemento è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento modificato nei membri **hItem**, **state**, **lParam** e **pszText.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE per** annullare la modifica delle etichette.

## <a name="remarks"></a>Commenti

Quando inizia la modifica delle etichette, un controllo di modifica viene creato ma non posizionato o visualizzato. Prima che venga visualizzato, il controllo di visualizzazione albero invia alla finestra padre un codice di notifica TVN \_ BEGINLABELEDIT.

Per personalizzare la modifica delle etichette, implementare un gestore per TVN BEGINLABELEDIT e fare in modo che invii un messaggio \_ [**\_ TVM GETEDITCONTROL**](tvm-geteditcontrol.md) al controllo di visualizzazione albero. Se un'etichetta viene modificata, il valore restituito sarà un handle per il controllo di modifica. Usare questo handle per personalizzare il controllo di modifica inviando i normali messaggi EM \_ XXX.

Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di notifica [ \_ TVN ENDLABELEDIT.](tvn-endlabeledit.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) e **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





