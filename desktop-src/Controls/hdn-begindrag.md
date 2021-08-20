---
title: HDN_BEGINDRAG di notifica (Commctrl.h)
description: Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno dei relativi elementi. Questo codice di notifica viene inviato solo dai controlli intestazione impostati sullo stile \_ HDS DRAGDROP. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae1ab3f8ac24b5521fab1afc5313503867e575906e851acf4d4fdbe90fe787d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544691"
---
# <a name="hdn_begindrag-notification-code"></a>Codice di notifica \_ HDN BEGINDRAG

Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno dei relativi elementi. Questo codice di notifica viene inviato solo dai controlli intestazione impostati sullo stile [**\_ HDS DRAGDROP.**](header-control-styles.md) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento di intestazione trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire al controllo intestazione di gestire automaticamente le operazioni di trascinamento della selezione, restituire **FALSE.** Se il proprietario del controllo esegue manualmente il riordinamento del trascinamento della selezione, restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un controllo intestazione gestisce automaticamente il riordinamento con trascinamento della selezione. La restituzione **di TRUE** per indicare la gestione del trascinamento della selezione esterna (manuale) consente al proprietario del controllo di fornire servizi personalizzati come parte del processo di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





