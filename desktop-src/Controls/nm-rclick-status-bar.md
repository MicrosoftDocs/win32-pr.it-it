---
title: NM_RCLICK di notifica (barra di stato) (Commctrl.h)
description: Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK di notifica (barra di stato) Windows controlli
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a42be8d41552173ef458d2f2c4e6232aa033aebfccd878142ac21b7f69f01b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799051"
---
# <a name="nm_rclick-status-bar-notification-code"></a>Codice di \_ notifica NM RCLICK (barra di stato)

Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per indicare che il clic del mouse è stato gestito ed elimina l'elaborazione predefinita da parte del sistema. Restituisce **FALSE per** consentire l'elaborazione predefinita del clic.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





