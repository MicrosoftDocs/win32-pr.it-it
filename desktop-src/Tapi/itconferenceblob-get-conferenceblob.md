---
description: Il \_ metodo Get ConferenceBlob ottiene un puntatore al BLOB di conferenza testuale attualmente archiviato nell'oggetto BLOB della conferenza.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Metodo ITConferenceBlob:: get_ConferenceBlob (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328235"
---
# <a name="itconferenceblobget_conferenceblob-method"></a>Metodo ITConferenceBlob:: Get \_ ConferenceBlob

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ ConferenceBlob** ottiene un puntatore al BLOB di conferenza testuale attualmente archiviato nell'oggetto BLOB della conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppBlob* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il BLOB della conferenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppBlob* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppBlob* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_set di caratteri BLOB \_**](blob-character-set.md)
</dt> </dl>

 

