---
title: Codice di notifica LBN_SELCHANGE (winuser. h)
description: Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Controlli di Windows per il codice di notifica LBN_SELCHANGE
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741570"
---
# <a name="lbn_selchange-notification-code"></a>\_Codice di notifica SelChange di LBN

Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da una casella di riepilogo con lo stile di [**\_ notifica lbs**](list-box-styles.md) .

Questo codice di notifica non viene inviato se il messaggio [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ secursel**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) o [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifica la selezione.

Per una casella di riepilogo a selezione multipla, \_ viene inviato il codice di notifica SelChange di LBN ogni volta che l'utente preme un tasto di direzione, anche se la selezione non cambia.

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

[**di \_ lb**](lb-setcursel.md)
</dt> <dt>

[\_DBLCLK LBN](lbn-dblclk.md)
</dt> <dt>

[\_SELCANCEL LBN](lbn-selcancel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

