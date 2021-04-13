---
description: Notifica alle applicazioni che si è verificato un evento di risparmio energia.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Messaggio WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529095"
---
# <a name="wm_powerbroadcast-message"></a>\_Messaggio POWERBROADCAST WM

Notifica alle applicazioni che si è verificato un evento di risparmio energia.

Una finestra riceve questo messaggio tramite la funzione **WindowProc** .


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

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>*uMsg*</dt> <dd> 

| Valore                                                                                                                                                                                                                                          | Significato                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>* * * * WM \_ POWERBROADCAST * *</dt> * * <dt>536 (0x218)</dt> </dl> | Identificatore del messaggio.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Evento di risparmio energia. Questo parametro può essere uno dei seguenti identificatori di evento.



| Evento                                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | Lo stato di alimentazione è stato modificato.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | L'operazione viene ripresa automaticamente da uno stato di basso consumo. Questo messaggio viene inviato ogni volta che il sistema riprende.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | Operazione ripresa da uno stato di basso consumo. Questo messaggio viene inviato dopo [ \_ APMRESUMEAUTOMATIC PBT](pbt-apmresumeautomatic.md) se il resume viene attivato dall'input dell'utente, ad esempio premendo un tasto.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | Il sistema sta per sospendere l'operazione.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | È stato ricevuto un evento di modifica dell'impostazione di risparmio energia. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dati specifici dell'evento. Per la maggior parte degli eventi, questo parametro è riservato e non viene utilizzato.

Se il parametro *wParam* è [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), il parametro *lParam* è un puntatore a una struttura di [**\_ impostazione POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire **true** se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Il sistema invia sempre un messaggio [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) ogni volta che il sistema riprende. Se il sistema riprende in risposta all'input dell'utente, ad esempio premendo un tasto, il sistema invia anche un messaggio **\_ APMRESUMESUSPEND PBT** dopo l'invio di \_ APMRESUMEAUTOMATIC PBT.

**WM \_** I messaggi POWERBROADCAST non fanno distinzione tra Stati a bassa potenza diversi. Un'applicazione può determinare solo che il sistema è in entrata o è stato ripreso da uno stato di basso consumo; non è in grado di determinare lo stato di alimentazione specifico. Il sistema registra informazioni dettagliate sulle transizioni di stato dell'alimentazione nel registro eventi di sistema di Windows.

Per impedire che il sistema passi a uno stato di basso consumo in Windows Vista, un'applicazione deve chiamare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per informare il sistema che è in uso.

I messaggi seguenti non sono supportati in nessuno dei sistemi operativi specificati nella sezione requisiti:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_Messaggi WM POWERBROADCAST](wm-powerbroadcast-messages.md)
</dt> <dt>

[Messaggi di risparmio energia](power-management-messages.md)
</dt> </dl>

 

 




