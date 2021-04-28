---
title: BN_DBLCLK di notifica (Winuser.h)
description: "BN_DBLCLK codice di notifica: inviato quando l'utente fa doppio clic su un pulsante."
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK codice di notifica controlli Windows
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
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096849"
---
# <a name="bn_dblclk-notification-code"></a>Codice di notifica \_ DBLCLK BN

Inviato quando l'utente fa doppio clic su un pulsante. Questo codice di notifica viene inviato automaticamente per i pulsanti [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)e [**BS \_ OWNERDRAW.**](button-styles.md) Gli altri tipi di pulsante inviano \_ BN DBLCLK solo se hanno lo [**stile BS \_ NOTIFY.**](button-styles.md)

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

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

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
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[BN \_ SU CUI È STATO FATTO CLIC](bn-clicked.md)
</dt> <dt>

[BN \_ DOUBLECLICKED](bn-doubleclicked.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

