---
description: Il metodo get \_ SessionId ottiene il valore NTP (Network Time Protocol) a 32 bit che funge da identificatore di sessione. Viene generato automaticamente quando viene creata la sessione.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: Metodo ITSdp::get_SessionId (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f7e8ea9bef17e5cb34ca23443b1f16f815c964c3cf76b9b122878e8662d051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621541"
---
# <a name="itsdpget_sessionid-method"></a>Metodo ITSdp::get \_ SessionId

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ SessionId** ottiene il valore NTP (Network Time Protocol) a 32 bit che funge da identificatore di sessione. Viene generato automaticamente quando viene creata la sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSessionId* \[ Cambio\]
</dt> <dd>

Puntatore all'identificatore di sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pSessionId* non è valido.<br/>             |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pSessionId* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo potrebbe **essere ULONG,** ma Visual Basic non supporta il **tipo ULONG.** Double **è** il tipo più piccolo successivo che include l'intero intervallo di valori necessari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




