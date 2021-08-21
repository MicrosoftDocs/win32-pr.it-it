---
title: LVN_DELETEALLITEMS di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che tutti gli elementi nel controllo stanno per essere eliminati. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f76ec4deaf67c1448fab5054c05ea8ede79c0972061c8be8e4f36b2e40ef54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019129"
---
# <a name="lvn_deleteallitems-notification-code"></a>Codice di notifica LVN \_ DELETEALLITEMS

Notifica alla finestra padre di un controllo visualizzazione elenco che tutti gli elementi nel controllo stanno per essere eliminati. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Il **membro iItem** è -1 e gli altri membri sono pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per eliminare i codici [di notifica \_ LVN DELETEITEM](lvn-deleteitem.md) successivi, restituire **TRUE.**

Per ricevere i codici [di notifica \_ LVN DELETEITEM](lvn-deleteitem.md) successivi, restituire **FALSE.**

## <a name="remarks"></a>Commenti

Un controllo di visualizzazione elenco invia il codice di notifica [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) quando viene eliminato definitivamente o quando riceve il messaggio **LVM \_ DELETEALLITEMS.** Se **LVM \_ DELETEALLITEMS** non restituisce **TRUE,** il controllo invierà anche un codice di notifica [LVN \_ DELETEITEM](lvn-deleteitem.md) quando ogni elemento viene eliminato.

Se il gestore di messaggi [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) si trova in una routine della finestra di dialogo, restituire **TRUE** dalla routine della finestra di dialogo e usare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL MSGRESULT per impostare il valore restituito del \_ messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

