---
title: TBN_BEGINDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a trascinare un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5283b2853709742713f79afb761cc39739f6df7467a1de869c545c705c8488ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077975"
---
# <a name="tbn_begindrag-notification-code"></a>Codice di notifica \_ TBN BEGINDRAG

Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a trascinare un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Il **membro iItem** contiene l'identificatore di comando del pulsante trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





