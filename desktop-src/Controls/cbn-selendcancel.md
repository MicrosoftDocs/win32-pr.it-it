---
title: Codice di notifica CBN_SELENDCANCEL (winuser. h)
description: Inviato quando l'utente seleziona un elemento, ma seleziona un altro controllo o chiude la finestra di dialogo. Indica che la selezione iniziale dell'utente deve essere ignorata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- Controlli di Windows per il codice di notifica CBN_SELENDCANCEL
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743047"
---
# <a name="cbn_selendcancel-notification-code"></a>\_Codice di notifica SELENDCANCEL CBN

Inviato quando l'utente seleziona un elemento, ma seleziona un altro controllo o chiude la finestra di dialogo. Indica che la selezione iniziale dell'utente deve essere ignorata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella combinata.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una casella combinata con lo [**stile \_ semplice CBS**](combo-box-styles.md) , il codice di notifica di CBN \_ SELENDCANCEL non viene inviato. Il codice di notifica di [CBN \_ SELENDOK](cbn-selendok.md) viene inviato immediatamente prima di ogni codice di notifica [ \_ selChange CBN](cbn-selchange.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[\_selChange CBN](cbn-selchange.md)
</dt> <dt>

[\_SELENDOK CBN](cbn-selendok.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

