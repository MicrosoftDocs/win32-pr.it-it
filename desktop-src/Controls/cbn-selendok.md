---
title: Codice di notifica CBN_SELENDOK (winuser. h)
description: Inviato quando l'utente seleziona una voce di elenco o seleziona un elemento e quindi lo chiude. Indica che la selezione dell'utente deve essere elaborata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Controlli di Windows per il codice di notifica CBN_SELENDOK
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301672"
---
# <a name="cbn_selendok-notification-code"></a>\_Codice di notifica SELENDOK CBN

Inviato quando l'utente seleziona una voce di elenco o seleziona un elemento e quindi lo chiude. Indica che la selezione dell'utente deve essere elaborata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDOK

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

In una casella combinata con lo [**stile \_ semplice CBS**](combo-box-styles.md) , il codice di notifica di CBN \_ SELENDOK viene inviato immediatamente prima di ogni codice di notifica [ \_ selChange CBN](cbn-selchange.md) .

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

[\_SELENDCANCEL CBN](cbn-selendcancel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

