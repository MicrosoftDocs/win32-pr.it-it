---
title: EN_ALIGNRTL di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è cambiata da destra a sinistra. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ COMMAND.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179b9a610d2d834081ddd246ea4d649c099a8df3a62d21815c825bd55701dad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799851"
---
# <a name="en_alignrtl-notification-code"></a>Codice di notifica EN \_ ALIGNRTL

Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è cambiata da destra a sinistra. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGNRTL

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

[**EN \_ ALIGNLTR**](en-alignltr.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

