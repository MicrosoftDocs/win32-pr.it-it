---
title: Messaggio WM_SETFOCUS (winuser. h)
description: Inviato a una finestra dopo che ha ottenuto lo stato attivo della tastiera.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Input della tastiera e del mouse WM_SETFOCUS messaggio
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478760"
---
# <a name="wm_setfocus-message"></a>Messaggio di SetFocus di WM \_

Inviato a una finestra dopo che ha ottenuto lo stato attivo della tastiera.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra che ha perso lo stato attivo della tastiera. Questo parametro può essere **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Per visualizzare un accento circonflesso, un'applicazione deve chiamare le funzioni del cursore appropriate quando riceve il messaggio **di \_ SetFocus di WM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**\_KILLFOCUS WM**](wm-killfocus.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

