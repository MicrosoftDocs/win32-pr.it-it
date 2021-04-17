---
description: Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Messaggio WM_DEVICECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401413"
---
# <a name="wm_devicechange-message"></a>\_Messaggio DEVICECHANGE WM

Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificatore **WM \_ DEVICECHANGE** .

</dd> <dt>

*wParam* 
</dt> <dd>

Evento che si è verificato. Questo parametro può essere uno dei valori seguenti del file di intestazione DBT. h.



| Valore                                                                                                                                                                                                                                                                                                  | Significato                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> CONFIGCHANGECANCELED </dl>             | Una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_](dbt-configchanged.md)**</dt> <dt>0x0018</dt> CONFIGCHANGED </dl>                                         | La configurazione corrente è cambiata a causa di un ancoraggio o di Undock.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_](dbt-customevent.md)**</dt> <dt>0x8006</dt> CUSTOMEVENT </dl>                                                 | Si è verificato un evento personalizzato.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> DEVICEARRIVAL </dl>                                         | Un dispositivo o un elemento multimediale è stato inserito ed è ora disponibile.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> DEVICEQUERYREMOVE </dl>                         | Viene richiesta l'autorizzazione per rimuovere un dispositivo o un elemento multimediale. Qualsiasi applicazione può negare questa richiesta e annullare la rimozione.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> DEVICEQUERYREMOVEFAILED </dl> | Una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> DEVICEREMOVECOMPLETE </dl>             | Un dispositivo o un elemento multimediale è stato rimosso.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> DEVICEREMOVEPENDING </dl>                 | Un dispositivo o un elemento multimediale sta per essere rimosso. Non può essere negato.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> DEVICETYPESPECIFIC </dl>                     | Si è verificato un evento specifico del dispositivo.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_ DEVNODE \_ modificato](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Un dispositivo è stato aggiunto o rimosso dal sistema.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> QUERYCHANGECONFIG </dl>                         | Viene richiesta l'autorizzazione per modificare la configurazione corrente (dock o Undock).<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> USERDEFINED </dl>                                                 | Il significato di questo messaggio è definito dall'utente.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene dati specifici dell'evento. Il formato dipende dal valore del parametro *wParam* . Per ulteriori informazioni, vedere la documentazione relativa a ogni evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per concedere la richiesta.

Restituisce **la \_ query broadcast \_ Deny** per negare la richiesta.

## <a name="remarks"></a>Commenti

Per i dispositivi che offrono funzionalità controllabili dal software, ad esempio l'espulsione e il blocco, il sistema invia in genere un messaggio [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) per consentire alle applicazioni e ai driver di dispositivo di terminare l'uso del dispositivo normalmente. Se il sistema rimuove forzatamente un dispositivo, è possibile che non invii un messaggio [ \_ DEVICEQUERYREMOVE di DBT](dbt-devicequeryremove.md) prima di procedere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                                             |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                                                    |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h o dbt. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_CONFIGCHANGECANCELED DBT](dbt-configchangecanceled.md)
</dt> <dt>

[\_CONFIGCHANGED DBT](dbt-configchanged.md)
</dt> <dt>

[\_CUSTOMEVENT DBT](dbt-customevent.md)
</dt> <dt>

[\_DEVICEARRIVAL DBT](dbt-devicearrival.md)
</dt> <dt>

[\_DEVICEQUERYREMOVE DBT](dbt-devicequeryremove.md)
</dt> <dt>

[\_DEVICEQUERYREMOVEFAILED DBT](dbt-devicequeryremovefailed.md)
</dt> <dt>

[\_DEVICEREMOVECOMPLETE DBT](dbt-deviceremovecomplete.md)
</dt> <dt>

[\_DEVICEREMOVEPENDING DBT](dbt-deviceremovepending.md)
</dt> <dt>

[\_DEVICETYPESPECIFIC DBT](dbt-devicetypespecific.md)
</dt> <dt>

[\_DEVNODE DBT \_ modificato](dbt-devnodes-changed.md)
</dt> <dt>

[\_QUERYCHANGECONFIG DBT](dbt-querychangeconfig.md)
</dt> <dt>

[\_USERDEFINED DBT](dbt-userdefined.md)
</dt> </dl>

 

