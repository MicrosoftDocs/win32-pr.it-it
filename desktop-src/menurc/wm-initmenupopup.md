---
title: Messaggio WM_INITMENUPOPUP (winuser. h)
description: Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- Menu del messaggio WM_INITMENUPOPUP e altre risorse
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
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048080"
---
# <a name="wm_initmenupopup-message"></a>\_Messaggio INITMENUPOPUP WM

Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.


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

La parola di ordine inferiore specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.

La parola più ordinata indica se il menu a discesa è il menu finestra. Se il menu è il menu finestra, questo parametro è **true**; in caso contrario, è **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

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

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_INITMENU WM**](wm-initmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

