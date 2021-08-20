---
description: Messaggio inviato ogni volta che viene apportata una modifica all'ora di sistema.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: WM_TIMECHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16829714ace9f2b8d0a038aff4410817a9ab43b9d6594b82344ecf8a7dbdc836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957321"
---
# <a name="wm_timechange-message"></a>Messaggio \_ WM TIMECHANGE

Messaggio inviato ogni volta che viene apportata una modifica all'ora di sistema.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

**WM \_ Identificatore TIMECHANGE.**

</dd> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Un'applicazione non deve trasmettere questo messaggio, perché il sistema trasmetterà questo messaggio quando l'applicazione modifica l'ora di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

