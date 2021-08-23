---
description: Il metodo get StartTime ottiene il valore dell'ora di inizio \_ NTP (Network Time Protocol) a 32 bit. La sessione viene considerata attiva da questo momento.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: Metodo ITTime::get_StartTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2fcc7aedf94d65f828714a7ebe5e6bbbfd760514654b2b634b479f2fd4802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060759"
---
# <a name="ittimeget_starttime-method"></a>Metodo ITTime::get \_ StartTime

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ StartTime** ottiene il valore dell'ora di inizio NTP (Network Time Protocol) a 32 bit. La sessione viene considerata attiva da questo momento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTime* \[ Cambio\]
</dt> <dd>

Puntatore all'ora di inizio della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pTime* non è un puntatore valido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

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

[**ITTime::put \_ StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




