---
description: Inviato quando un'applicazione modifica lo stato di abilitazione di una finestra.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Messaggio WM_ENABLE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314870"
---
# <a name="wm_enable-message"></a>\_Messaggio di abilitazione WM

Inviato quando un'applicazione modifica lo stato di abilitazione di una finestra. Viene inviata alla finestra il cui stato abilitato è in corso di modifica. Questo messaggio viene inviato prima della restituzione della funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , ma dopo la modifica dello stato abilitato ([**WS \_ disabled**](window-styles.md) Style bit) della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se la finestra è stata abilitata o disabilitata. Questo parametro è **true** se la finestra è stata abilitata o **false** se la finestra è stata disabilitata.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
