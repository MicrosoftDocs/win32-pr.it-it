---
title: BCN_DROPDOWN di notifica (Winuser.h)
description: Inviato quando l'utente fa clic su una freccia a discesa su un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbacf22cdabbac7c5d2932c604fab634dbc185207acda8cee311d434478e5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674973"
---
# <a name="bcn_dropdown-notification-code"></a>Codice di notifica \_ BCN DROPDOWN

Inviato quando l'utente fa clic su una freccia a discesa su un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) Il **membro rcButton** è impostato per descrivere l'area a discesa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast **di LPARAM** per recuperare [**la struttura NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) **WPARAM** contiene l'ID del controllo che invia il messaggio. Il controllo pulsante deve avere uno stile di pulsante a discesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





