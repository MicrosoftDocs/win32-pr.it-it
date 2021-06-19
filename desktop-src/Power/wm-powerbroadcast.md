---
description: Notifica alle applicazioni che si è verificato un evento di risparmio energia.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST messaggio (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396506"
---
# <a name="wm_powerbroadcast-message"></a>Messaggio \_ DI WM POWERBROADCAST

Notifica alle applicazioni che si è verificato un evento di risparmio energia.

Una finestra riceve questo messaggio tramite la **relativa funzione WindowProc.**


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
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

| Valore                                                                                                                                                                                                                                          | Significato                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>****WM \_ POWERBROADCAST****</dt> <dt>536 (0x218)</dt> </dl> | Identificatore del messaggio.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Evento di risparmio energia. Questo parametro può essere uno degli identificatori di evento seguenti.



| Evento                                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | Lo stato dell'alimentazione è cambiato.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | L'operazione viene ripresa automaticamente da uno stato a basso consumo. Questo messaggio viene inviato ogni volta che il sistema riprende.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | L'operazione viene ripresa da uno stato a basso consumo. Questo messaggio viene inviato dopo [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) se il ripresa viene attivato dall'input dell'utente, ad esempio premendo un tasto.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | Il sistema sta sospendendo l'operazione.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | È stato ricevuto un evento di modifica dell'impostazione di risparmio energia. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dati specifici dell'evento. Per la maggior parte degli eventi, questo parametro è riservato e non utilizzato.

Se il *parametro wParam* è [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), il *parametro lParam* è un puntatore a una [**struttura \_ SETTING di POWERBROADCAST.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve **restituire TRUE** se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Il sistema invia sempre un [messaggio \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) ogni volta che il sistema riprende. Se il sistema riprende in risposta all'input dell'utente, ad esempio premendo un tasto, il sistema invia anche un messaggio **PBT \_ APMRESUMESUSPEND** dopo l'invio di PBT \_ APMRESUMEAUTOMATIC.

**WM \_ I messaggi POWERBROADCAST** non distinguono tra diversi stati a basso consumo. Un'applicazione può determinare solo che il sistema sta entrando o è ripreso da uno stato a basso consumo. non è in grado di determinare lo stato di alimentazione specifico. Il sistema registra informazioni dettagliate sulle transizioni dello stato di alimentazione nel registro eventi di sistema di Windows.

Per impedire al sistema di passare a uno stato a basso consumo in Windows Vista, un'applicazione deve chiamare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per informare il sistema che è in uso.

I messaggi seguenti non sono supportati in nessuno dei sistemi operativi specificati nella sezione Requisiti:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi \_ WM POWERBROADCAST](wm-powerbroadcast-messages.md)
</dt> <dt>

[Messaggi di risparmio energia](power-management-messages.md)
</dt> </dl>

 

 




