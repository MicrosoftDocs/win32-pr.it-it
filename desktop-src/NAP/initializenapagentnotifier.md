---
title: Funzione InitializeNapAgentNotifier (NapUtil. h)
description: Sottoscrive il processo chiamante per NapAgent le notifiche di modifica dello stato e la quarantena delle notifiche di modifica dello stato.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- NAP funzione InitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964003"
---
# <a name="initializenapagentnotifier-function"></a>InitializeNapAgentNotifier (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **InitializeNapAgentNotifier** sottoscrive il processo chiamante per napagent le notifiche di modifica dello stato e la quarantena delle notifiche di modifica dello stato. Queste notifiche vengono fornite dal servizio NapAgent.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da ricevere.

</dd> <dt>

*hNotifyEvent* \[ in\]
</dt> <dd>

Handle di evento utilizzato per la notifica. Il chiamante deve passare un handle aperto al parametro *hNotifyEvent* . Il chiamante deve anche chiudere l'handle di evento quando non è più necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                                | Descrizione                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Inizializzazione completata.<br/>                                                         |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                     | Inizializzazione non riuscita.<br/>                                                                         |
| <dl> <dt>**ERRORE \_ già \_ inizializzato**</dt> </dl> | Il processo ha già sottoscritto le notifiche del servizio NapAgent del *tipo* specificato. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | È stato passato un argomento non valido. <br/>                                                               |



 

## <a name="remarks"></a>Commenti

Questa funzione non è thread-safe.

Ogni processo che richiede una sottoscrizione per le notifiche del servizio NapAgent del *tipo* specificato deve chiamare **InitializeNapAgentNotifier** per sottoscrivere le notifiche. Se un processo deve sottoscrivere più di un tipo di notifica, deve chiamare **InitializeNapAgentNotifier** una volta per ogni tipo di notifica.

Quando un processo non richiede ulteriori notifiche, il processo deve chiamare [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) per il *tipo* specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





