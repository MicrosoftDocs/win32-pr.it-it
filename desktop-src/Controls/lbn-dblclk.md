---
title: LBN_DBLCLK di notifica (Winuser.h)
description: Notifica all'applicazione che l'utente ha fatto doppio clic su un elemento in una casella di riepilogo. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- LBN_DBLCLK del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132e1b68527aca9227702caeea40ffd8deb46e375ffdd87bcf1288dfb01584e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085311"
---
# <a name="lbn_dblclk-notification-code"></a>Codice di \_ notifica LBN DBLCLK

Notifica all'applicazione che l'utente ha fatto doppio clic su un elemento in una casella di riepilogo. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da una casella di riepilogo con lo stile L [**BS \_ NOTIFY.**](button-styles.md)

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

[LBN \_ SELCHANGE](lbn-selchange.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

