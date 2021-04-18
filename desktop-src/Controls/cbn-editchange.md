---
title: Codice di notifica CBN_EDITCHANGE (winuser. h)
description: Inviato dopo che l'utente ha eseguito un'azione che potrebbe aver modificato il testo nella parte del controllo di modifica di una casella combinata.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- Controlli di Windows per il codice di notifica CBN_EDITCHANGE
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302645"
---
# <a name="cbn_editchange-notification-code"></a>\_Codice di notifica EDITCHANGE CBN

Inviato dopo che l'utente ha eseguito un'azione che potrebbe aver modificato il testo nella parte del controllo di modifica di una casella combinata. A differenza del codice di notifica di [CBN \_ EDITUPDATE](cbn-editupdate.md) , questo codice di notifica viene inviato dopo che il sistema ha aggiornato la schermata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_EDITCHANGE

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

Se la casella combinata ha lo stile di [**\_ DropDownList CBS**](combo-box-styles.md) , questo codice di notifica non viene inviato.

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

[\_EDITUPDATE CBN](cbn-editupdate.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

