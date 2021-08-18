---
title: NM_KEYDOWN di notifica (Commctrl.h)
description: "NM_KEYDOWN di notifica: inviato da un controllo quando il controllo ha lo stato attivo e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio WM \\_ NOTIFY."
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c68dd0eaa82d8a8687aaadaa195e4fba121e7db84031eefe1404ad387748580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958100"
---
# <a name="nm_keydown-notification-code"></a>Codice \_ di notifica NM KEYDOWN

Inviato da un controllo quando il controllo ha lo stato attivo e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire al controllo di elaborare il tasto oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





