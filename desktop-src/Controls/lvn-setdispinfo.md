---
title: Codice di notifica LVN_SETDISPINFO (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che deve aggiornare le informazioni gestite per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Controlli di Windows per il codice di notifica LVN_SETDISPINFO
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964572"
---
# <a name="lvn_setdispinfo-notification-code"></a>\_Codice di notifica SETDISPINFO di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che deve aggiornare le informazioni gestite per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) che specifica le informazioni per l'elemento modificato. Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene informazioni sull'elemento che è stato modificato. Il membro **pszText** dell' **elemento** contiene un valore valido, indipendentemente dal fatto che il \_ flag di testo LVIF sia impostato nel membro **mask** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Il parametro *wParam* contiene il codice del messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_GETDISPINFO LVN](lvn-getdispinfo.md)
</dt> </dl>

 

 





