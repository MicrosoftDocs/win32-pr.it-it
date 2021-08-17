---
title: NM_RELEASEDCAPTURE (barra degli strumenti) codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo barra degli strumenti che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- NM_RELEASEDCAPTURE di notifica (barra degli strumenti) Windows controlli
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
ms.openlocfilehash: 5df364d5a303ca5b62a435710c32cee5aa1e7bae7dc5c0f800c23c058b4dcfb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957970"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>Codice di notifica NM \_ RELEASEDCAPTURE (barra degli strumenti)

Notifica alla finestra padre di un controllo barra degli strumenti che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





