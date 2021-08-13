---
description: Il metodo get SessionVersion ottiene il valore \_ a 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: Metodo ITSdp::get_SessionVersion (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476591"
---
# <a name="itsdpget_sessionversion-method"></a>Metodo ITSdp::get \_ SessionVersion

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ SessionVersion** ottiene il valore a 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione. Anche se viene generato automaticamente quando viene creata la sessione, l'utente è responsabile della modifica quando viene modificato il SDP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSessionVersion* \[ Cambio\]
</dt> <dd>

Puntatore all'identificatore di versione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pSessionVersion* non è valido.<br/>           |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pSessionVersion* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                     |



 

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo può essere **ULONG,** ma Visual Basic non supporta il **tipo ULONG.** Double **è** il tipo più piccolo successivo che include l'intero intervallo di valori necessari.

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
</dt> <dt>

[**ITSdp::put \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




