---
title: Codice di notifica EN_SETFOCUS (winuser. h)
description: Inviato quando un controllo di modifica riceve lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Controlli di Windows per il codice di notifica EN_SETFOCUS
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743034"
---
# <a name="en_setfocus-notification-code"></a>\_Codice di notifica di SetFocus

Inviato quando un controllo di modifica riceve lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La finestra padre riceve sempre un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[EN \_ KILLFOCUS](en-killfocus.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

