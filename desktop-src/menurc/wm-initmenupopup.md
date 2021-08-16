---
title: WM_INITMENUPOPUP messaggio (Winuser.h)
description: "WM_INITMENUPOPUP messaggio: inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu."
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869600"
---
# <a name="wm_initmenupopup-message"></a>Messaggio \_ WM INITMENUPOPUP

Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il menu a discesa o il sottomenu.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola meno ordinata specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.

La parola più importante indica se il menu a discesa è il menu della finestra. Se il menu è il menu della finestra, questo parametro è **TRUE**; in caso contrario, è **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

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

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ INITMENU**](wm-initmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

