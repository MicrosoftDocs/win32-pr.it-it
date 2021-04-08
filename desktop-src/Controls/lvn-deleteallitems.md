---
title: Codice di notifica LVN_DELETEALLITEMS (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che tutti gli elementi del controllo stanno per essere eliminati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Controlli di Windows per il codice di notifica LVN_DELETEALLITEMS
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
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965016"
---
# <a name="lvn_deleteallitems-notification-code"></a>\_Codice di notifica DELETEALLITEMS di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che tutti gli elementi del controllo stanno per essere eliminati. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Il membro **iItem** è-1 e gli altri membri sono pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per visualizzare i codici di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) successivi, restituire **true**.

Per ricevere i codici di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) successivi, restituire **false**.

## <a name="remarks"></a>Commenti

Un controllo elenco-visualizzazione Invia il codice di notifica [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) quando viene eliminato definitivamente o quando riceve il messaggio **LVM \_ DELETEALLITEMS** . Se **LVM \_ DELETEALLITEMS** non restituisce **true**, il controllo invierà anche un codice di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) quando ogni elemento viene eliminato.

Se il gestore di messaggi [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) si trova in una routine della finestra di dialogo, restituire **true** dalla routine della finestra di dialogo e utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT per impostare il valore restituito del messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

