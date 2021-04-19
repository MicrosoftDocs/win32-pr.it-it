---
description: Il \_ metodo Get SessionVersion ottiene il valore 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Metodo ITSdp:: get_SessionVersion (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333958"
---
# <a name="itsdpget_sessionversion-method"></a>Metodo ITSdp:: Get \_ SessionVersion

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ SessionVersion** ottiene il valore 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione. Sebbene venga generato automaticamente quando viene creata la sessione, l'utente è responsabile della sua modifica quando il SDP viene modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSessionVersion* \[ out\]
</dt> <dd>

Puntatore all'identificatore della versione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pSessionVersion* non è valido.<br/>           |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pSessionVersion* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>    |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                     |



 

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo potrebbe essere **ULONG**, ma Visual Basic non supporta il tipo **ULONG** . Un **Double** è il tipo più piccolo successivo che comprende l'intero intervallo di valori necessari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::p UT \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




