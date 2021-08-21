---
title: Funzione InitializeNapAgentNotifier (NapUtil.h)
description: Sottoscrive il processo chiamante per le notifiche di modifica dello stato napAgent e le notifiche di modifica dello stato di quarantena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Funzione InitializeNapAgentNotifier NAP
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
ms.openlocfilehash: 1ac2d874f6138bcc1fbc97952d4464e56e05b0a497c7b0ff98e9c05e8c8434e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133456"
---
# <a name="initializenapagentnotifier-function"></a>Funzione InitializeNapAgentNotifier

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione InitializeNapAgentNotifier** sottoscrive il processo chiamante per le notifiche di modifica dello stato di NapAgent e le notifiche di modifica dello stato di quarantena. Queste notifiche vengono fornite dal servizio NapAgent.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da ricevere.

</dd> <dt>

*hNotifyEvent* \[ Pollici\]
</dt> <dd>

Handle di evento utilizzato per la notifica. Il chiamante deve passare un handle aperto al *parametro hNotifyEvent.* Il chiamante deve anche chiudere l'handle dell'evento quando non è più necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                                | Descrizione                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Inizializzazione completata.<br/>                                                         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Inizializzazione non riuscita.<br/>                                                                         |
| <dl> <dt>**ERRORE \_ GIÀ \_ INIZIALIZZATO**</dt> </dl> | Il processo ha già sottoscritto le notifiche del servizio NapAgent del *tipo* specificato. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | È stato passato un argomento non valido. <br/>                                                               |



 

## <a name="remarks"></a>Commenti

Questa funzione non è thread-safe.

Ogni processo che richiede una sottoscrizione alle  notifiche del servizio NapAgent del tipo specificato deve chiamare **InitializeNapAgentNotifier** per sottoscrivere le notifiche. Se un processo deve sottoscrivere più di un tipo di notifica, deve chiamare **InitializeNapAgentNotifier** una volta per ogni tipo di notifica.

Quando un processo non richiede altre notifiche, deve chiamare [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) per il tipo *specificato.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





