---
description: Il metodo Init inizializza il BLOB della conferenza in base a una stringa testuale. Se pBlob è NULL, vengono usati i valori predefiniti.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: Metodo ITConferenceBlob::Init (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4f7816d1de346e12b3fab799728f32fb146664846d9dcb6d7cd7df757d62e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991931"
---
# <a name="itconferenceblobinit-method"></a>Metodo ITConferenceBlob::Init

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Init** inizializza il BLOB della conferenza in base a una stringa testuale. Se *pBlob* è **NULL,** vengono usati i valori predefiniti.

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

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una **rappresentazione BSTR** del nome della conferenza.

</dd> <dt>

*Set di caratteri* \[ Pollici\]
</dt> <dd>

[**BLOB \_ Descrittore \_ CHARACTER SET**](blob-character-set.md) del set di caratteri.

</dd> <dt>

*pBlob* \[ Pollici\]
</dt> <dd>

Puntatore a un **oggetto BSTR contenente** il BLOB della conferenza. Se **NULL,** il BLOB della conferenza viene inizializzato con i valori predefiniti. Attualmente, i valori predefiniti della conferenza sono disponibili solo se il *parametro CharacterSet* è impostato su BCS \_ ASCII.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pName,* *CharacterSet* o *pBlob* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>            |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                             |



 

## <a name="remarks"></a>Commenti

**ITConferenceBlob::Init** restituirà un errore se il BLOB è già stato inizializzato.

L'applicazione deve [**usare SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per i *parametri pName* *e pBlob.* L'applicazione deve [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando le variabili non sono più necessarie.

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

 

