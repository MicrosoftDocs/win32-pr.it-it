---
title: LVN_ITEMCHANGED di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che un elemento è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED del codice di notifica Windows controlli
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
ms.openlocfilehash: bea129a1b62b442b0fb545f29a57e9eab0d6d1bae057996df5bc269d9a4296d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830385"
---
# <a name="lvn_itemchanged-notification-code"></a>Codice di notifica LVN \_ ITEMCHANGED

Notifica alla finestra padre di un controllo visualizzazione elenco che un elemento è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quali attributi sono stati modificati. Se il **membro iItem** della struttura a cui *punta lParam* è -1, la modifica è stata applicata a tutti gli elementi nella visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se un controllo visualizzazione elenco ha lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) e l'utente seleziona un intervallo di elementi tenendo premuto MAIUSC e facendo clic con il mouse, i codici di notifica LVN ITEMCHANGED non vengono inviati per ogni elemento selezionato o \_ deselezionato. Si riceverà invece un singolo codice di notifica [LVN \_ ODSTATECHANGED,](lvn-odstatechanged.md) che indica che lo stato di un intervallo di elementi è cambiato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





