---
title: BN_SETFOCUS di notifica (Winuser.h)
description: Inviato quando un pulsante riceve lo stato attivo della tastiera. Per inviare questo codice di notifica, il pulsante deve avere lo stile \_ BS NOTIFY. La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a10cb9b728d6f98f984ff6b70fb76c42102d8414d486cdba3db27b3ac6fbe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827591"
---
# <a name="bn_setfocus-notification-code"></a>Codice di notifica \_ BN SETFOCUS

Inviato quando un pulsante riceve lo stato attivo della tastiera. Per inviare questo codice di notifica, il pulsante deve avere lo stile [**\_ BS NOTIFY.**](button-styles.md)

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_SETFOCUS

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

[BN \_ KILLFOCUS](bn-killfocus.md)
</dt> </dl>

 

