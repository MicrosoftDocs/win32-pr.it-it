---
description: Inviato prima del messaggio WM \_ CREATE quando viene creata una finestra per la prima volta.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa5638ef1b97365d202f2049fc79712d0ed3eec167825110f7c7967ce4605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200057"
---
# <a name="wm_nccreate-message"></a>Messaggio \_ WM NCCREATE

Inviato prima del [**messaggio WM \_ CREATE**](wm-create.md) quando viene creata una finestra per la prima volta.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Puntatore alla [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) che contiene informazioni sulla finestra da creare. I membri **di CREATESTRUCT** sono identici ai parametri della [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire **TRUE per** continuare la creazione della finestra. Se l'applicazione **restituisce FALSE,** la [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) restituirà un handle **NULL.**

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

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
