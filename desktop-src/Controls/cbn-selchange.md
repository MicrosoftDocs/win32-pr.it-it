---
title: CBN_SELCHANGE codice di notifica (Winuser.h)
description: Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f808438f8592acfdede592fab352bbeb0dd7123b5dc41db86eadb6749ae8b4ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968621"
---
# <a name="cbn_selchange-notification-code"></a>Codice di notifica \_ CBN SELCHANGE

Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata. L'utente può modificare la selezione facendo clic nella casella di riepilogo o usando i tasti di direzione. La finestra padre della casella combinata riceve questo codice di notifica sotto forma di messaggio [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella combinata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ottenere l'indice della selezione corrente, inviare il messaggio [**\_ GETCURSEL CB**](cb-getcursel.md) al controllo.

Il codice di notifica CBN SELCHANGE non viene inviato quando la selezione corrente \_ viene impostata usando il [**messaggio \_ CB SETCURSEL.**](cb-setcursel.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[CBN \_ CLOSEUP](cbn-closeup.md)
</dt> <dt>

[CBN \_ DBLCLK](cbn-dblclk.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

