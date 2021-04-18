---
description: Inviato prima del messaggio di \_ creazione di WM quando una finestra viene creata per la prima volta.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Messaggio WM_NCCREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312368"
---
# <a name="wm_nccreate-message"></a>\_Messaggio NCCREATE WM

Inviato prima del messaggio [**di \_ creazione di WM**](wm-create.md) quando una finestra viene creata per la prima volta.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) che contiene informazioni sulla finestra da creare. I membri di **struttura CREATESTRUCT** sono identici ai parametri della funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire **true** per continuare la creazione della finestra. Se l'applicazione restituisce **false**, la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) restituirà un handle **null** .

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**STRUTTURA CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**creazione di WM \_**](wm-create.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
