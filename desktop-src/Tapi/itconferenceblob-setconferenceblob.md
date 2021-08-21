---
description: Il metodo SetConferenceBlob esegue il commit delle modifiche nel BLOB della conferenza. Per inizializzare il BLOB della conferenza per la prima volta, usare invece il metodo Init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: Metodo ITConferenceBlob::SetConferenceBlob (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 391a20ade99d3e35da9d4f76eaab13b6ba65b07b5693321c6c3b2bb63f53c2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865425"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>Metodo ITConferenceBlob::SetConferenceBlob

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo SetConferenceBlob** esegue il commit delle modifiche nel BLOB della conferenza. Per inizializzare il BLOB della conferenza per la prima volta, usare invece il [**metodo Init.**](itconferenceblob-init.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Set di caratteri* \[ Pollici\]
</dt> <dd>

[**BLOB \_ Descrittore \_ CHARACTER SET**](blob-character-set.md) del set di caratteri del BLOB della conferenza.

</dd> <dt>

*pBlob* \[ Pollici\]
</dt> <dd>

Puntatore a un **oggetto BSTR contenente** il BLOB della conferenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro CharacterSet* *o pBlob* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pBlob* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

 

