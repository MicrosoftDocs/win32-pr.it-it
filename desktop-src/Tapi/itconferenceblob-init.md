---
description: Il metodo init Inizializza il BLOB della conferenza in base a una stringa testuale. Se pBlob è NULL, vengono usati i valori predefiniti.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Metodo ITConferenceBlob:: init (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328232"
---
# <a name="itconferenceblobinit-method"></a>Metodo ITConferenceBlob:: init

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **init** Inizializza il BLOB della conferenza in base a una stringa testuale. Se *pBlob* è **null**, vengono usati i valori predefiniti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una rappresentazione **BSTR** del nome della conferenza.

</dd> <dt>

*Carattere* \[ in\]
</dt> <dd>

[**BLOB \_ \_**](blob-character-set.md) Descrittore del set di caratteri del set di caratteri.

</dd> <dt>

*pBlob* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il BLOB della conferenza. Se **null**, il BLOB della conferenza viene inizializzato con i valori predefiniti. Attualmente, i valori di conferenza predefiniti sono disponibili solo se il parametro del set di *caratteri* è impostato su BCS \_ ASCII.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pname*, *charactert* o *pBlob* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>            |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                             |



 

## <a name="remarks"></a>Commenti

**ITConferenceBlob:: init** restituirà un errore se il BLOB è già stato inizializzato.

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per i parametri *pname* e *pBlob* . L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando le variabili non sono più necessarie.

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

 

