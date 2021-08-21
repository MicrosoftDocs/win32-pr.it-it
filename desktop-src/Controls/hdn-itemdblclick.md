---
title: HDN_ITEMDBLCLICK codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo intestazione che l'utente ha fatto doppio clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY. Solo i controlli intestazione impostati sullo stile HDS \_ BUTTONS inviano questo codice di notifica.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544613"
---
# <a name="hdn_itemdblclick-notification-code"></a>Codice di \_ notifica HDN ITEMDBLCLICK

Notifica alla finestra padre di un controllo intestazione che l'utente ha fatto doppio clic sul controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) Solo i controlli intestazione impostati sullo stile [**HDS \_ BUTTONS**](header-control-styles.md) inviano questo codice di notifica.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





