---
title: IPN_FIELDCHANGED di notifica (Commctrl.h)
description: Inviato quando l'utente modifica un campo nel controllo o si sposta da un campo a un altro. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED codice di notifica Windows controlli
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
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085551"
---
# <a name="ipn_fieldchanged-notification-code"></a>Codice di notifica FIELDCHANGED IPN \_

Inviato quando l'utente modifica un campo nel controllo o si sposta da un campo a un altro. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) che contiene informazioni sull'indirizzo modificato. Il **membro iValue** di questa struttura conterrà il valore immesso, anche se non è compreso nell'intervallo del campo. È possibile modificare questo membro in qualsiasi valore compreso nell'intervallo per il campo in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica non viene inviato in risposta a un [**messaggio \_ IPM SETADDRESS.**](ipm-setaddress.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





