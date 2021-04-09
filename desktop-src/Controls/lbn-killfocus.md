---
title: Codice di notifica LBN_KILLFOCUS (winuser. h)
description: Notifica all'applicazione che la casella di riepilogo ha perso lo stato attivo della tastiera. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- Controlli di Windows per il codice di notifica LBN_KILLFOCUS
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba424efc2518d359c3d031561aeafee8c0348b65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120995"
---
# <a name="lbn_killfocus-notification-code"></a>\_Codice di notifica KILLFOCUS di LBN

Notifica all'applicazione che la casella di riepilogo ha perso lo stato attivo della tastiera. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

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

[LBN \_ SetFocus](lbn-setfocus.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

