---
title: EN_ALIGNLTR di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è cambiata da sinistra a destra. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ COMMAND.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 884f2750501dc1670d2f8e0497a196276571328809d295a687b3518a34b38ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019449"
---
# <a name="en_alignltr-notification-code"></a>Codice di notifica EN \_ ALIGNLTR

Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è cambiata da sinistra a destra. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EN \_ ALIGNRTL**](en-alignrtl.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

