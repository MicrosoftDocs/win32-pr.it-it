---
title: LVN_SETDISPINFO codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che deve aggiornare le informazioni mantenute per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO codice di notifica Windows controlli
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
ms.openlocfilehash: 6f4827d37a115f2bd1bb523f78bdb5975de4314056a174be4bfa886e1a076497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915061"
---
# <a name="lvn_setdispinfo-notification-code"></a>Codice di notifica \_ LVN SETDISPINFO

Notifica alla finestra padre di un controllo visualizzazione elenco che deve aggiornare le informazioni mantenute per un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) che specifica le informazioni per l'elemento modificato. Il **membro** elemento di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene informazioni sull'elemento modificato. Il **membro pszText** dell'elemento contiene un valore valido, indipendentemente dal fatto che il flag LVIF TEXT sia impostato nel membro  \_ **mask** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast *di lParam* per recuperare la [**struttura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Il *parametro wParam* contiene il codice del messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





