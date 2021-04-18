---
description: Il \_ metodo Get charactert ottiene un \_ \_ descrittore del set di caratteri BLOB del set di caratteri usato nel BLOB della conferenza corrente.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Metodo ITConferenceBlob:: get_CharacterSet (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328236"
---
# <a name="itconferenceblobget_characterset-method"></a>Metodo ITConferenceBlob:: Get \_ charactert

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ charactert** ottiene un descrittore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) del set di caratteri usato nel BLOB della conferenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCharacterSet* \[ out\]
</dt> <dd>

Puntatore a un descrittore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) del set di caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                   | Descrizione                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>                     | Il parametro *pCharacterSet* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>                 | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Questo metodo non è ancora implementato.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* è **null**.<br/>                          |
| <dl> <dt>**HRESULT ERRORE \_ dati non validi \_**</dt> </dl> | Il set di caratteri corrente non è valido o non è disponibile.<br/>  |



 

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

 

 




