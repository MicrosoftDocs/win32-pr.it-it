---
title: CBN_DROPDOWN di notifica (Winuser.h)
description: Inviato quando la casella di riepilogo di una casella combinata sta per essere resa visibile. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978ac01818f3e9ed7da9f3f1decc7398ab4af32df8f884041bec327640a8014d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438301"
---
# <a name="cbn_dropdown-notification-code"></a>Codice di notifica A DISCESA CBN \_

Inviato quando la casella di riepilogo di una casella combinata sta per essere resa visibile. La finestra padre della casella combinata riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_DROPDOWN

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

Questo codice di notifica viene inviato solo se la casella combinata ha lo stile [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

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

[CBN \_ CLOSEUP](cbn-closeup.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

