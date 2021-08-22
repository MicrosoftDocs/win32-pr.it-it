---
description: Il metodo get \_ CharacterSet ottiene un \_ descrittore BLOB CHARACTER \_ SET del set di caratteri usato nel BLOB della conferenza corrente.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: Metodo ITConferenceBlob::get_CharacterSet (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060999"
---
# <a name="itconferenceblobget_characterset-method"></a>Metodo ITConferenceBlob::get \_ CharacterSet

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ CharacterSet** ottiene un [**\_ descrittore BLOB CHARACTER \_ SET**](blob-character-set.md) del set di caratteri usato nel BLOB della conferenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCharacterSet* \[ Cambio\]
</dt> <dd>

Puntatore a [**un \_ descrittore BLOB CHARACTER \_ SET**](blob-character-set.md) del set di caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                   | Descrizione                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>                     | Il *parametro pCharacterSet* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | Memoria insufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Questo metodo non è ancora implementato.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* è **NULL.**<br/>                          |
| <dl> <dt>**(HRESULT) ERRORE \_ DATI NON \_ VALIDI**</dt> </dl> | Il set di caratteri corrente non è valido o non è disponibile.<br/>  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**SET \_ DI CARATTERI \_ BLOB**](blob-character-set.md)
</dt> </dl>

 

 




