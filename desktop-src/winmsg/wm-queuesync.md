---
description: Inviato da un'applicazione di training basata su computer (CBT) per separare i messaggi di input dell'utente da altri messaggi inviati tramite la \_ procedura WH JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Messaggio WM_QUEUESYNC (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312366"
---
# <a name="wm_queuesync-message"></a>\_Messaggio QUEUESYNC WM

Inviato da un'applicazione di training basata su computer (CBT) per separare i messaggi di input dell'utente da altri messaggi inviati tramite la procedura [**WH \_ JOURNALPLAYBACK**](about-hooks.md) .


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **void**

Un'applicazione CBT deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Ogni volta che un'applicazione CBT usa la procedura [**WH \_ JOURNALPLAYBACK**](about-hooks.md) , il primo e l'ultimo messaggio sono **WM \_ QUEUESYNC**. Ciò consente all'applicazione CBT di intercettare ed esaminare i messaggi avviati dall'utente senza eseguire questa operazione per gli eventi inviati.

Se un'applicazione specifica un handle di finestra **null** , il messaggio viene inserito nella coda di messaggi della finestra attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Hook](hooks.md)
</dt> </dl>

 

 
