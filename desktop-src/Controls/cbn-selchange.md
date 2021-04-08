---
title: Codice di notifica CBN_SELCHANGE (winuser. h)
description: Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- Controlli di Windows per il codice di notifica CBN_SELCHANGE
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
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964942"
---
# <a name="cbn_selchange-notification-code"></a>\_Codice di notifica SelChange CBN

Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata. L'utente può modificare la selezione facendo clic nella casella di riepilogo o usando i tasti di direzione. La finestra padre della casella combinata riceve questo codice di notifica sotto forma di un messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELCHANGE

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

Per ottenere l'indice della selezione corrente, inviare il messaggio del [**CB \_ GetCurSel**](cb-getcursel.md) al controllo.

Il codice di notifica di CBN \_ selChange non viene inviato quando la selezione corrente viene impostata usando il messaggio di [**\_ malmaledizione CB**](cb-setcursel.md) .

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

[primo piano CBN \_](cbn-closeup.md)
</dt> <dt>

[\_DBLCLK CBN](cbn-dblclk.md)
</dt> <dt>

[**CB \_ GETcursel**](cb-getcursel.md)
</dt> <dt>

[**\_CAcursel CB**](cb-setcursel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

