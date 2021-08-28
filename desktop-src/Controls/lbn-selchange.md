---
title: LBN_SELCHANGE codice di notifica (Winuser.h)
description: Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE codice di notifica Windows controlli
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
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085181"
---
# <a name="lbn_selchange-notification-code"></a>Codice di notifica \_ LBN SELCHANGE

Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da una casella di riepilogo con lo [**stile \_ LBS NOTIFY.**](list-box-styles.md)

Questo codice di notifica non viene inviato se il messaggio [**LB \_ SETSEL,**](lb-setsel.md) [**LB \_ SETCURSEL,**](lb-setcursel.md) [**LB \_ SELECTSTRING,**](lb-selectstring.md) [**LB \_ SELITEMRANGE**](lb-selitemrange.md) o [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifica la selezione.

Per una casella di riepilogo a selezione multipla, il codice di notifica LBN SELCHANGE viene inviato ogni volta che l'utente preme un tasto di direzione, anche se la selezione \_ non cambia.

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

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

