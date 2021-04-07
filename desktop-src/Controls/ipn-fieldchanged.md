---
title: Codice di notifica IPN_FIELDCHANGED (COMmctrl. h)
description: Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Controlli di Windows per il codice di notifica IPN_FIELDCHANGED
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048611"
---
# <a name="ipn_fieldchanged-notification-code"></a>Codice di notifica di IPN \_ FIELDCHANGED

Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) che contiene informazioni sull'indirizzo modificato. Il membro **iValue** della struttura conterrà il valore immesso, anche se non è compreso nell'intervallo del campo. È possibile modificare questo membro in qualsiasi valore compreso nell'intervallo per il campo in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica non viene inviato in risposta a un messaggio di [**\_ Indirizzo IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





