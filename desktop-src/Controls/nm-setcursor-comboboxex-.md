---
title: NM_SETCURSOR di notifica (ComboBoxEx) (Commctrl.h)
description: Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un messaggio WM \_ SETCURSOR. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR di notifica (ComboBoxEx) Windows controlli
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0f7c7ffc8459ae1da279b6e53329f894662dd6ae6f30888fd9bdbdf631fa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798991"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>Codice di notifica NM \_ SETCURSOR (ComboBoxEx)

Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un [**messaggio WM \_ SETCURSOR.**](/windows/desktop/menurc/wm-setcursor) Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per consentire al controllo di impostare il cursore o un valore diverso da zero per impedire al controllo di impostare il cursore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

