---
title: NM_DBLCLK (visualizzazione albero) codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic sul pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- NM_DBLCLK di notifica (visualizzazione albero) Windows controlli
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c18fa9409365aa55b2410f16ae51ddbdcc1113c730b11293f997e1c641277c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088791"
---
# <a name="nm_dblclk-tree-view-notification-code"></a>Codice di notifica NM \_ DBLCLK (visualizzazione albero)

Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic sul pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





