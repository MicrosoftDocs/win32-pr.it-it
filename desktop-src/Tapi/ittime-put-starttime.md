---
description: Il metodo put StartTime imposta il valore dell'ora di inizio \_ NTP (Network Time Protocol) a 32 bit. La sessione viene considerata attiva a partire da questo momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: Metodo ITTime::p ut_StartTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e1fe25f2518396ec507f88d0a89c5928f676b64d626c32307336b95ef21e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003229"
---
# <a name="ittimeput_starttime-method"></a>Metodo ITTime::p ut \_ StartTime

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo put \_ StartTime** imposta il valore dell'ora di inizio NTP (Network Time Protocol) a 32 bit. La sessione viene considerata attiva a partire da questo momento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ora* \[ Pollici\]
</dt> <dd>

Ora di inizio della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Tim* e non è valido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questa funzione può inviare dati in modalità non crittografata. Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Prima di usare questo metodo, è consigliabile considerare il rischio di sicurezza di inviare i dati in testo non crittografato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::get \_ StartTime**](ittime-get-starttime.md)
</dt> </dl>

 

 




