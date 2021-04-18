---
title: Codice di notifica EN_ALIGNRTL (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è stata modificata da destra a sinistra. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di comando WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- Controlli di Windows per il codice di notifica EN_ALIGNRTL
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
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476096"
---
# <a name="en_alignrtl-notification-code"></a>\_Codice di notifica en ALIGNRTL

Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è stata modificata da destra a sinistra. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



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

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

