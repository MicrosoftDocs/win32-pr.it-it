---
title: Codice di notifica BN_DBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic su un pulsante.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Controlli di Windows per il codice di notifica BN_DBLCLK
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048129"
---
# <a name="bn_dblclk-notification-code"></a>\_Codice di notifica DBLCLK BN

Inviato quando l'utente fa doppio clic su un pulsante. Questo codice di notifica viene inviato automaticamente per i pulsanti [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) . Altri tipi di pulsante inviano BN \_ DBLCLK solo se hanno lo stile di [**\_ notifica BS**](button-styles.md) .

La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

BN \_ DBLCLK è uguale al codice di notifica con [ \_ doppio clic di BN](bn-doubleclicked.md) .

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

[BN \_ selezionato](bn-clicked.md)
</dt> <dt>

[MILIARDI di \_ DoubleClick](bn-doubleclicked.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

