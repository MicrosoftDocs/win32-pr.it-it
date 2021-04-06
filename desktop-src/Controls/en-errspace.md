---
title: Codice di notifica EN_ERRSPACE (winuser. h)
description: Inviato quando un controllo di modifica non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- Controlli di Windows per il codice di notifica EN_ERRSPACE
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873386"
---
# <a name="en_errspace-notification-code"></a>\_Codice di notifica en ERRSPACE

Inviato quando un controllo di modifica non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ERRSPACE

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

La finestra padre otterrà sempre un messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) per questo evento e non richiede una maschera di notifica inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

