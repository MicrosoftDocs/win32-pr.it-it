---
title: Codice di notifica BN_SETFOCUS (winuser. h)
description: Inviato quando un pulsante riceve lo stato attivo della tastiera. Il pulsante deve avere lo \_ stile di notifica BS per inviare il codice di notifica. La finestra padre del pulsante riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- Controlli di Windows per il codice di notifica BN_SETFOCUS
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
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301183"
---
# <a name="bn_setfocus-notification-code"></a>Codice di notifica per la messa a fuoco di BN \_

Inviato quando un pulsante riceve lo stato attivo della tastiera. Il pulsante deve avere lo stile di [**\_ notifica BS**](button-styles.md) per inviare il codice di notifica.

La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[BN \_ KILLFOCUS](bn-killfocus.md)
</dt> </dl>

 

