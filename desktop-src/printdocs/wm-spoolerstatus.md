---
description: Il messaggio WM SPOOLERSTATUS viene inviato da Print Manager ogni volta che un processo viene aggiunto o rimosso \_ dalla coda di Gestione stampa.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2869c468517abf466b348583748e391fc1f2a4226c74b5811fffabdb5eeb89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460341"
---
# <a name="wm_spoolerstatus-message"></a>Messaggio \_ SPOOLERSTATUS WM

Il **messaggio \_ WM SPOOLERSTATUS** viene inviato da Print Manager ogni volta che un processo viene aggiunto o rimosso dalla coda di Gestione stampa.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*wParam* 
</dt> <dd>

Flag \_ JOBSTATUS della richiesta pull.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa specifica il numero di processi rimanenti nella coda di Gestione stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio è solo a scopo informativo. Questo messaggio è consultivo e non ha una semantica di recapito garantita. Le applicazioni non devono presupporre che riceveranno un messaggio \_ SPOOLERSTATUS WM per ogni modifica dello stato dello spooler.

Il messaggio \_ WM SPOOLERSTATUS non è supportato dopo Windows XP. Per ricevere una notifica delle modifiche apportate allo stato della coda di stampa, è possibile usare [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) e [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Messaggi dell'API Spooler di stampa](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

