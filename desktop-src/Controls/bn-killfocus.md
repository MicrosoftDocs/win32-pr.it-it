---
title: BN_KILLFOCUS di notifica (Winuser.h)
description: Inviato quando un pulsante perde lo stato attivo della tastiera. Per inviare questo codice di notifica, il pulsante deve avere lo stile \_ BS NOTIFY. La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f312ba2282c72b7db30c170b44528bd469591bbb0a4b4a2e14bb797d2be67f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674087"
---
# <a name="bn_killfocus-notification-code"></a>Codice di notifica \_ BN KILLFOCUS

Inviato quando un pulsante perde lo stato attivo della tastiera. Per inviare questo codice di notifica, il pulsante deve avere lo stile [**\_ BS NOTIFY.**](button-styles.md)

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[BN \_ SETFOCUS](bn-setfocus.md)
</dt> </dl>

 

