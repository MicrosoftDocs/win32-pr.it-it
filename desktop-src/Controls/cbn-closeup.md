---
title: Codice di notifica CBN_CLOSEUP (winuser. h)
description: Inviato quando la casella di riepilogo di una casella combinata è stata chiusa. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- Controlli di Windows per il codice di notifica CBN_CLOSEUP
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121614"
---
# <a name="cbn_closeup-notification-code"></a>\_Codice di notifica primo piano CBN

Inviato quando la casella di riepilogo di una casella combinata è stata chiusa. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_CLOSEUP

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

Se l'utente ha modificato la selezione corrente, la casella combinata invia anche il codice di notifica di [CBN \_ selChange](cbn-selchange.md) quando l'elenco a discesa viene chiuso. In generale, non è possibile prevedere l'ordine in cui verranno inviati i codici di notifica. In particolare, un \_ codice di notifica SelChange CBN può verificarsi prima o dopo un \_ codice di notifica primo piano CBN.

Per eseguire un processo specifico ogni volta che l'utente seleziona una voce di elenco, è possibile gestire il codice di notifica di [CBN \_ selChange](cbn-selchange.md) o CBN \_ closeup. In genere, è possibile attendere il \_ codice di notifica primo piano CBN prima di elaborare una modifica nella selezione corrente. Questo può essere particolarmente importante se è necessaria una quantità significativa di elaborazione.

Questo codice di notifica non viene inviato a una casella combinata con stile [**\_ semplice CBS**](combo-box-styles.md) .

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

[\_elenco a discesa CBN](cbn-dropdown.md)
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

 

