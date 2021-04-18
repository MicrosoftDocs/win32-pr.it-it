---
title: Codice di notifica LVN_ITEMCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302799"
---
# <a name="lvn_itemchanged-notification-code"></a>\_Codice di notifica ITEMCHANGED di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quali attributi sono stati modificati. Se il membro **iItem** della struttura a cui punta *lParam* è-1, la modifica è stata applicata a tutti gli elementi nella visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se un controllo di visualizzazione elenco ha lo [**stile \_ OWNERDATA LVS**](list-view-window-styles.md) e l'utente seleziona un intervallo di elementi tenendo premuto il tasto MAIUSC e facendo clic sul mouse, i \_ codici di notifica LVN ITEMCHANGED non vengono inviati per ogni elemento selezionato o deselezionato. Si riceverà invece un solo codice di notifica [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) , che indica che un intervallo di elementi è stato modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





