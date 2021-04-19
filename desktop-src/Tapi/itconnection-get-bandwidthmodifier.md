---
description: Il \_ metodo Get BandwidthModifier ottiene il modificatore della larghezza di banda, ovvero una singola parola alfanumerica che fornisce il significato della figura della larghezza di banda. I due modificatori definiti sono CT (Total Conference) e AS (valore massimo specifico dell'applicazione).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Metodo ITConnection:: get_BandwidthModifier (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326512"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a>Metodo ITConnection:: Get \_ BandwidthModifier

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ BandwidthModifier** ottiene il modificatore della larghezza di banda, ovvero una singola parola alfanumerica che fornisce il significato della figura della larghezza di banda. I due modificatori definiti sono CT (Total Conference) e AS (valore massimo specifico dell'applicazione).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppModifier* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il modificatore della larghezza di banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppModifier* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppModifier* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

