---
title: BN_DBLCLK di notifica (Winuser.h)
description: "BN_DBLCLK di notifica: inviato quando l'utente fa doppio clic su un pulsante."
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK del codice di notifica Windows controlli
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
ms.openlocfilehash: 7a80886811a5fcc91f4f0a1217754fdd1daf0cca5b39c1158235d77351008788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674355"
---
# <a name="bn_dblclk-notification-code"></a>Codice di notifica \_ BN DBLCLK

Inviato quando l'utente fa doppio clic su un pulsante. Questo codice di notifica viene inviato automaticamente per i pulsanti [**\_ BS USERBUTTON**](button-styles.md), [**BS \_ RADIOBUTTON**](button-styles.md)e [**BS \_ OWNERDRAW.**](button-styles.md) Gli altri tipi di pulsante inviano DBLCLK BN \_ solo se hanno lo stile [**BS \_ NOTIFY.**](button-styles.md)

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) l'identificatore del controllo del pulsante. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

BN \_ DBLCLK corrisponde al codice di notifica [BN \_ DOUBLECLICKED.](bn-doubleclicked.md)

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

[CLIC \_ SU BN](bn-clicked.md)
</dt> <dt>

[BN \_ DOUBLECLICKED](bn-doubleclicked.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

