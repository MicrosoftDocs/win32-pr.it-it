---
title: EN_ERRSPACE di notifica (Winuser.h)
description: Inviato quando un controllo di modifica non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio WM \_ COMMAND.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE del codice di notifica Windows controlli
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
ms.openlocfilehash: 548270e6382befa8a202a94c625f8cea214025d41661305f290250d66a771cbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047771"
---
# <a name="en_errspace-notification-code"></a>Codice di notifica EN \_ ERRSPACE

Inviato quando un controllo di modifica non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La finestra padre riceverà sempre un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) per questo evento. Non richiede una maschera di notifica inviata con il messaggio [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

