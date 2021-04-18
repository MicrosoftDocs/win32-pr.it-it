---
title: Codice di notifica BCN_DROPDOWN (winuser. h)
description: Inviato quando l'utente fa clic su una freccia a discesa di un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di un messaggio di \_ notifica WM.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- Controlli di Windows per il codice di notifica BCN_DROPDOWN
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
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301396"
---
# <a name="bcn_dropdown-notification-code"></a>\_Codice di notifica a discesa BCN

Inviato quando l'utente fa clic su una freccia a discesa di un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di un messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . Il membro **rcButton** è impostato in modo da descrivere l'area a discesa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . **WParam** contiene l'ID del controllo che invia questo messaggio. Il controllo Button deve avere uno stile del pulsante a discesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





