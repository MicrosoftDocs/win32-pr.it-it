---
title: NM_RCLICK di notifica (scheda) (Commctrl.h)
description: Notifica alla finestra padre di un controllo struttura a schede che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- NM_RCLICK di notifica (scheda) Windows controlli
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
ms.openlocfilehash: 5f873074cb5827af4c974ec8d0a064552279b5f48625b725b09c426d8d63fd79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958230"
---
# <a name="nm_rclick-tab-notification-code"></a>Codice di \_ notifica NM RCLICK (scheda)

Notifica alla finestra padre di un controllo struttura a schede che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per non consentire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





