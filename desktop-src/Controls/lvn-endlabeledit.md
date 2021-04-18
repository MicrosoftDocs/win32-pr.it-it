---
title: Codice di notifica LVN_ENDLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Controlli di Windows per il codice di notifica LVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302803"
---
# <a name="lvn_endlabeledit-notification-code"></a>\_Codice di notifica ENDLABELEDIT di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui membro **iItem** identifica l'elemento da modificare. Il membro **pszText** dell' **elemento** contiene un valore valido quando \_ viene inviato il codice di notifica ENDLABELEDIT LVN, indipendentemente dal fatto che il \_ flag di testo LVIF sia impostato nel membro **mask** della struttura **LVITEM** . Se l'utente annulla la modifica, il membro **pszText** della struttura **LVITEM** è **null**. in caso contrario, **pszText** è l'indirizzo del testo modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) è diverso da **null**, restituisce **true** per impostare l'etichetta dell'elemento sul testo modificato. Restituisce **false** per rifiutare il testo modificato e ripristinare l'etichetta originale.

Se il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) è **null**, il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Il valore restituito dalla routine della finestra di dialogo indica se il messaggio è stato gestito. Il secondo valore restituito deve essere impostato chiamando [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) con **DWLP_MSGRESULT**.

Quando l'utente inizia a modificare l'etichetta di un elemento, la finestra padre del controllo elenco-visualizzazione riceve un codice di notifica [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) . Quando l'utente annulla o completa la modifica, la finestra padre riceve un \_ codice di notifica ENDLABELEDIT LVN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) e **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





