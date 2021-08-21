---
title: WM_SETFOCUS messaggio (Winuser.h)
description: Inviato a una finestra dopo aver ottenuto lo stato attivo della tastiera.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS messaggio Input da tastiera e mouse
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
ms.openlocfilehash: e7ba202a4f0205a28d294d2d4f54372921205ebb72516f6f26c4042e08d9cfe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757374"
---
# <a name="wm_setfocus-message"></a>Messaggio \_ WM SETFOCUS

Inviato a una finestra dopo aver ottenuto lo stato attivo della tastiera.


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

Per visualizzare un punto di accesso, un'applicazione deve chiamare le funzioni del punto di controllo appropriate quando riceve il **messaggio WM \_ SETFOCUS.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Setfocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ KILLFOCUS**](wm-killfocus.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

