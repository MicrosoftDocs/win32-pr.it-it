---
description: Il \_ messaggio WM DEVMODECHANGE viene inviato a tutte le finestre di primo livello ogni volta che l'utente modifica le impostazioni della modalità dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Messaggio WM_DEVMODECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980290"
---
# <a name="wm_devmodechange-message"></a>\_Messaggio DEVMODECHANGE WM

Il messaggio **WM \_ DEVMODECHANGE** viene inviato a tutte le finestre di primo livello ogni volta che l'utente modifica le impostazioni della modalità dispositivo.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle di una finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

\_DEVMODECHANGE WM

</dd> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa che specifica il nome del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Impossibile inviare questo messaggio direttamente a una finestra. Per inviare il messaggio **WM \_ DEVMODECHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con il parametro *HWND* impostato su HWND \_ broadcast.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei contesti di dispositivo](device-contexts.md)
</dt> <dt>

[Messaggi di contesto dispositivo](device-context-messages.md)
</dt> </dl>

 

 
