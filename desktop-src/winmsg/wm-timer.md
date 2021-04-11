---
description: Inserito nella coda di messaggi del thread di installazione quando scade un timer. Il messaggio viene inserito dalla funzione GetMessage o PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Messaggio WM_TIMER (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233016"
---
# <a name="wm_timer-message"></a>\_Messaggio timer WM

Inserito nella coda di messaggi del thread di installazione quando scade un timer. Il messaggio viene inserito dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Identificatore del timer.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una funzione di callback definita dall'applicazione passata alla funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante l'installazione del timer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

È possibile elaborare il messaggio fornendo un caso **del \_ timer WM** nella procedura della finestra. In caso contrario, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chiamerà la funzione di callback [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) specificata nella chiamata alla funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) utilizzata per installare il timer.

Il messaggio del **\_ timer WM** è un messaggio con priorità bassa. Le funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pubblicano questo messaggio solo quando non sono presenti altri messaggi con priorità più elevata nella coda di messaggi del thread.

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Timer](timers.md)
</dt> </dl>

 

 
