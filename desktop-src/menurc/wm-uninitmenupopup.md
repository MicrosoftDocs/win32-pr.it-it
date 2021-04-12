---
title: Messaggio WM_UNINITMENUPOPUP (winuser. h)
description: Inviato quando un menu a discesa o un sottomenu viene eliminato definitivamente.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- Menu del messaggio WM_UNINITMENUPOPUP e altre risorse
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
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519190"
---
# <a name="wm_uninitmenupopup-message"></a>\_Messaggio UNINITMENUPOPUP WM

Inviato quando un menu a discesa o un sottomenu viene eliminato definitivamente.


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

La parola più ordinata identifica il menu che è stato eliminato definitivamente. Attualmente, questo parametro può essere solo **MF \_ SYSMENU** (il menu finestra).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un'applicazione riceve un messaggio [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , riceverà un messaggio **WM \_ UNINITMENUPOPUP** .

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

