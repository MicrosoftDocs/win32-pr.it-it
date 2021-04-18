---
title: Codice di notifica CBN_DBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic su una stringa nella casella di riepilogo di una casella combinata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- Controlli di Windows per il codice di notifica CBN_DBLCLK
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302724"
---
# <a name="cbn_dblclk-notification-code"></a>\_Codice di notifica DBLCLK CBN

Inviato quando l'utente fa doppio clic su una stringa nella casella di riepilogo di una casella combinata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_DBLCLK

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

Questo codice di notifica si verifica solo per una casella combinata con stile [**\_ semplice CBS**](combo-box-styles.md) . In una casella combinata con l'elenco a [**\_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) , un doppio clic non può verificarsi perché un solo clic chiude la casella di riepilogo.

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

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

