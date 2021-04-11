---
description: Il \_ messaggio WM SPOOLERSTATUS viene inviato da Gestione stampa ogni volta che un processo viene aggiunto o rimosso dalla coda di Print Manager.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Messaggio WM_SPOOLERSTATUS (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131802"
---
# <a name="wm_spoolerstatus-message"></a>\_Messaggio SPOOLERSTATUS WM

Il messaggio **WM \_ SPOOLERSTATUS** viene inviato da Gestione stampa ogni volta che un processo viene aggiunto o rimosso dalla coda di Print Manager.

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

*wParam* 
</dt> <dd>

Flag JOBSTATUS della richiesta pull \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa indica il numero di processi rimanenti nella coda del gestore di stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio è esclusivamente a scopo informativo. Questo messaggio è consultivo e non ha una semantica di recapito garantita. Le applicazioni non devono presupporre che ricevano un \_ messaggio WM SPOOLERSTATUS per ogni modifica dello stato dello spooler.

Il \_ messaggio WM SPOOLERSTATUS non è supportato dopo Windows XP. Per ricevere una notifica delle modifiche apportate allo stato della coda di stampa, è possibile usare [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) e [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Messaggi dell'API spooler di stampa](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

