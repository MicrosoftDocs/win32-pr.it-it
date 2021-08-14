---
title: NM_RELEASEDCAPTURE codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 222a3be1-20f1-43c6-b982-852512209a45
keywords:
- NM_RELEASEDCAPTURE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2513ad413b5d4be8de3aa38b7b031b69d36ce017c9567cd9f0d85f5f05dfd80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986361"
---
# <a name="nm_releasedcapture-notification-code"></a>Codice di notifica NM \_ RELEASEDCAPTURE

Notifica alla finestra padre di un controllo che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non diversamente specificato, il controllo ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





