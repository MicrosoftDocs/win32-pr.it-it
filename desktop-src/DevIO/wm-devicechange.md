---
description: Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581503"
---
# <a name="wm_devicechange-message"></a>Messaggio \_ DEVICECHANGE WM

Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Identificatore **\_ DEVICECHANGE WM.**

</dd> <dt>

*wParam* 
</dt> <dd>

Evento che si è verificato. Questo parametro può essere uno dei valori seguenti del file di intestazione Dbt.h.

| Valore | Significato |
|-------|---------|
| **[DBT \_ DEVNODES \_ MODIFICATO](dbt-devnodes-changed.md)**</br>0x0007 | Un dispositivo è stato aggiunto o rimosso dal sistema. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | È richiesta l'autorizzazione per modificare la configurazione corrente (ancora o disanco). |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | La configurazione corrente è stata modificata a causa di un'ancoraggio o un disinseramento. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Una richiesta di modifica della configurazione corrente (ancora o disanco) è stata annullata. |
| **[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</br>0x8000 | Un dispositivo o un elemento multimediale è stato inserito ed è ora disponibile. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | È richiesta l'autorizzazione per rimuovere un dispositivo o un elemento multimediale. Qualsiasi applicazione può rifiutare questa richiesta e annullare la rimozione. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Un dispositivo o un elemento multimediale sta per essere rimosso. Non può essere negato. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Un dispositivo o un elemento multimediale è stato rimosso. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Si è verificato un evento specifico del dispositivo. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Si è verificato un evento personalizzato. |
| **[DBT \_ USERDEFINED](dbt-userdefined.md)**</br>0xFFFF | Il significato di questo messaggio è definito dall'utente. |

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene dati specifici dell'evento. Il formato dipende dal valore del *parametro wParam.* Per altre informazioni, vedere la documentazione per ogni evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire **TRUE per** concedere la richiesta.

Restituisce **BROADCAST \_ QUERY \_ DENY** per negare la richiesta.

## <a name="remarks"></a>Commenti

Per i dispositivi che offrono funzionalità di controllo software, ad esempio l'espulsione e il blocco, il sistema in genere invia un messaggio [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) per consentire alle applicazioni e ai driver di dispositivo di terminare normalmente l'uso del dispositivo. Se il sistema rimuove forzatamente un dispositivo, potrebbe non inviare un [messaggio DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) prima di eseguire questa operazione.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows XP |
| Server minimo supportato | Windows Server 2003|
| Intestazione | <dl> <dt>Winuser.h (includere Windows.h o Dbt.h)</dt> </dl> |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ MODIFICATO](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ DEFINITO DALL'UTENTE](dbt-userdefined.md)
</dt> </dl>
