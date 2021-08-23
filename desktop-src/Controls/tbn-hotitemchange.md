---
title: TBN_HOTITEMCHANGE codice di notifica (Commctrl.h)
description: Inviato da un controllo della barra degli strumenti quando cambia l'elemento di accesso rapido (evidenziato). Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51765a3c0590b4584b817772cec73df626363dfce6a5ef472ceec6c3ea023f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167039"
---
# <a name="tbn_hotitemchange-notification-code"></a>Codice di notifica \_ TBN HOTITEMCHANGE

Inviato da un controllo della barra degli strumenti quando cambia l'elemento di accesso rapido (evidenziato). Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire all'elemento di essere evidenziato o diverso da zero per impedire che l'elemento venga evidenziato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





