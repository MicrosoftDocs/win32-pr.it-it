---
title: WM_UNINITMENUPOPUP messaggio (Winuser.h)
description: Inviato quando un menu a discesa o un sottomenu è stato eliminato.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971790"
---
# <a name="wm_uninitmenupopup-message"></a>Messaggio \_ WM UNINITMENUPOPUP

Inviato quando un menu a discesa o un sottomenu è stato eliminato.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il menu

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più alta identifica il menu eliminato. Attualmente, questo parametro può essere solo **MF \_ SYSMENU** (il menu della finestra).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un'applicazione riceve un [**messaggio \_ WM INITMENUPOPUP,**](wm-initmenupopup.md) riceverà un messaggio **WM \_ UNINITMENUPOPUP.**

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

