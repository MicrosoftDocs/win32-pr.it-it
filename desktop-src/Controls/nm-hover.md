---
title: NM_HOVER codice di notifica (Commctrl.h)
description: Inviato da un controllo quando il puntatore del mouse viene posizionato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- NM_HOVER del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f5d1332c54328fba1b09ecf4efd48011edbe9a81139f05ad375fb6c8b070de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088701"
---
# <a name="nm_hover-notification-code"></a>Codice \_ di notifica DI NM HOVER

Inviato da un controllo quando il puntatore del mouse viene posizionato su un elemento. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non diversamente specificato, restituire zero per consentire al controllo di elaborare il passaggio del mouse normalmente o diverso da zero per impedire l'elaborazione del passaggio del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





