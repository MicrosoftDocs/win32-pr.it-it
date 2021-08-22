---
title: CBN_SELENDCANCEL di notifica (Winuser.h)
description: Inviato quando l'utente seleziona un elemento, ma quindi seleziona un altro controllo o chiude la finestra di dialogo. Indica che la selezione iniziale dell'utente deve essere ignorata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL del codice di notifica Windows controlli
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
ms.openlocfilehash: 869168bfb970df9afc6399e6b1ec40e02b9ccdeaa2f2fef93fcbd86c16e9c6d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314401"
---
# <a name="cbn_selendcancel-notification-code"></a>Codice di notifica \_ CBN SELENDCANCEL

Inviato quando l'utente seleziona un elemento, ma quindi seleziona un altro controllo o chiude la finestra di dialogo. Indica che la selezione iniziale dell'utente deve essere ignorata. La finestra padre della casella combinata riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella combinata.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una casella combinata con lo [**stile CBS \_ SIMPLE,**](combo-box-styles.md) il codice di notifica CBN \_ SELENDCANCEL non viene inviato. Il [codice di notifica \_ CBN SELENDOK](cbn-selendok.md) viene inviato immediatamente prima di ogni codice di notifica [ \_ CBN SELCHANGE.](cbn-selchange.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDOK](cbn-selendok.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

