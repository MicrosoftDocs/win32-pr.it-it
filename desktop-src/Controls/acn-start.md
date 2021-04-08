---
title: Codice di notifica ACN_START (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di animazione che è iniziata la riproduzione del clip AVI associato. Questo codice di notifica viene inviato sotto forma di un \_ messaggio di comando WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Controlli di Windows per il codice di notifica ACN_START
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740519"
---
# <a name="acn_start-notification-code"></a>\_Codice di notifica di avvio ACN

Notifica alla finestra padre di un controllo di animazione che è iniziata la riproduzione del clip AVI associato. Questo codice di notifica viene inviato sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo dell'animazione. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** che specifica l'handle per il controllo dell'animazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

