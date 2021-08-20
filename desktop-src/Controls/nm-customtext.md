---
title: NM_CUSTOMTEXT codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo le operazioni di testo personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512ccb6cd94ce680b9832c342696941d98c0e6543c319caeb89eb409de1fe73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018875"
---
# <a name="nm_customtext-notification-code"></a>Codice \_ di notifica NM CUSTOMTEXT

Notifica alla finestra padre di un controllo le operazioni di testo personalizzate. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





