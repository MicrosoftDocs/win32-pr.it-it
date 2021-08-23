---
title: NM_RELEASEDCAPTURE di notifica (trackbar) (Commctrl.h)
description: Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 1e3e4f67-672d-4e3e-84f4-b3fa6221d118
keywords:
- NM_RELEASEDCAPTURE di notifica (trackbar) Windows controlli
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
ms.openlocfilehash: f987ba9aec66a2a637736cb1b675196538ec46c7401b9a6317e5458a0bba7c48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957950"
---
# <a name="nm_releasedcapture-trackbar-notification-code"></a>Codice di notifica NM \_ RELEASEDCAPTURE (trackbar)

Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





