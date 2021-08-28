---
description: Inviato alla coda di messaggi del thread di installazione alla scadenza di un timer. Il messaggio viene pubblicato dalla funzione GetMessage o PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710031"
---
# <a name="wm_timer-message"></a>Messaggio WM \_ TIMER

Inviato alla coda di messaggi del thread di installazione alla scadenza di un timer. Il messaggio viene pubblicato dalla [**funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea)


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Identificatore del timer.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una funzione di callback definita dall'applicazione passata alla [**funzione SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) quando è stato installato il timer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

È possibile elaborare il messaggio specificando un case **WM \_ TIMER** nella routine della finestra. In caso [**contrario, DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chiamerà la funzione di callback [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) specificata nella chiamata alla [**funzione SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) usata per installare il timer.

Il **messaggio WM \_ TIMER** è un messaggio con priorità bassa. Le [**funzioni GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**e PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pubblicano questo messaggio solo quando nella coda di messaggi del thread non sono presenti altri messaggi con priorità più alta.

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

 

 
