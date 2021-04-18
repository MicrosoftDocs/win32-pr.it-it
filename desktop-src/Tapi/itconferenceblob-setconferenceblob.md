---
description: Il metodo SetConferenceBlob consente di eseguire il commit delle modifiche apportate al BLOB della conferenza. Per inizializzare il BLOB della conferenza per la prima volta, usare invece il metodo init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Metodo ITConferenceBlob:: SetConferenceBlob (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328230"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>Metodo ITConferenceBlob:: SetConferenceBlob

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetConferenceBlob** consente di eseguire il commit delle modifiche apportate al BLOB della conferenza. Per inizializzare il BLOB della conferenza per la prima volta, usare invece il metodo [**init**](itconferenceblob-init.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Carattere* \[ in\]
</dt> <dd>

[**BLOB \_ \_**](blob-character-set.md) Descrittore del set di caratteri del set di caratteri del BLOB della conferenza.

</dd> <dt>

*pBlob* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il BLOB della conferenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *charactert* o *pBlob* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PBlob* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

 

