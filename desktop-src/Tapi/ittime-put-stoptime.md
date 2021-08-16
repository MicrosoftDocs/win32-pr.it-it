---
description: Il metodo put StopTime imposta il valore dell'ora di fine \_ NTP (Network Time Protocol). Se l'ora di fine è zero, la sessione non è vincolata.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: Metodo ITTime::p ut_StopTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3aa32615988e52ccaa845a8fb7ec52f2e863c7193ee393d7d184e2b3002f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762383"
---
# <a name="ittimeput_stoptime-method"></a>Metodo ITTime::p ut \_ StopTime

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo put \_ StopTime** imposta il valore dell'ora di fine NTP (Network Time Protocol). Se l'ora di fine è zero, la sessione non è vincolata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ora* \[ Pollici\]
</dt> <dd>

Ora di arresto per la sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Time* non è valido.<br/>                   |
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

[**ITTime::get \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




