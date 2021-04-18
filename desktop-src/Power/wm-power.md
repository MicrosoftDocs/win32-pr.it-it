---
description: Notifica alle applicazioni che il sistema, in genere un personal computer alimentato dalla batteria, sta per entrare in modalità sospesa.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Messaggio WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312005"
---
# <a name="wm_power-message"></a>\_Power Message di WM

Notifica alle applicazioni che il sistema, in genere un personal computer alimentato dalla batteria, sta per entrare in modalità sospesa.

> [!Note]  
> Il messaggio di **\_ risparmio energia WM** è obsoleto. Viene fornita solo per la compatibilità con le applicazioni basate su Windows a 16 bit. Le applicazioni devono usare il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .

 

Una finestra riceve questo messaggio tramite la funzione **WindowProc** .


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificatore del messaggio di **\_ alimentazione WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Notifica degli eventi di alimentazione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**\_CRITICALRESUME PWR**</dt> </dl> | Indica che il sistema sta riprendendo l'operazione dopo l'attivazione della modalità sospesa senza prima trasmettere un messaggio di notifica **PWR \_ SUSPENDREQUEST** all'applicazione. Un'applicazione deve eseguire tutte le azioni di ripristino necessarie.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**\_SUSPENDREQUEST PWR**</dt> </dl> | Indica che il sistema sta per attivare la modalità sospesa.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**\_SUSPENDRESUME PWR**</dt> </dl>    | Indica che il sistema sta riprendendo l'operazione dopo che è stata attivata la modalità sospesa normalmente, il sistema trasmette un messaggio di notifica **PWR \_ SUSPENDREQUEST** all'applicazione prima che il sistema sia stato sospeso. Un'applicazione deve eseguire tutte le azioni di ripristino necessarie.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito da un'applicazione dipende dal valore del parametro *wParam* . Se *wParam* è **PWR \_ SUSPENDREQUEST**, il valore restituito è **PWR \_ non riesce** a impedire che il sistema entri nello stato Suspended. in caso contrario, è **PWR \_ OK**. Se *wParam* è **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME**, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Questo messaggio viene trasmesso solo a un'applicazione in esecuzione in un sistema conforme alla specifica del BIOS (Basic Input/Output System) di Advanced Power Management (APM). Il messaggio viene trasmesso dal driver di gestione del risparmio energia a ogni finestra restituita dalla funzione **EnumWindows** .

La modalità sospesa è lo stato in cui si verifica la maggiore quantità di risparmio energia, ma vengono conservati tutti i dati e i parametri operativi. Il contenuto della memoria ad accesso casuale (RAM) viene mantenuto, ma è probabile che molti dispositivi siano spenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




