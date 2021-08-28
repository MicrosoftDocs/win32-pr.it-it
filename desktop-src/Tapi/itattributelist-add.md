---
description: Il metodo Add aggiunge l'attributo in corrispondenza dell'indice specificato.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: Metodo ITAttributeList::Add (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9817fa413234f2eb2fa9bfb84f87ad794549443b5f807d743fa22805c30d9b49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905941"
---
# <a name="itattributelistadd-method"></a>Metodo ITAttributeList::Add

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Add** aggiunge l'attributo in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Indice dell'attributo da aggiungere.

</dd> <dt>

*pAttribute* \[ Pollici\]
</dt> <dd>

Puntatore a **un oggetto BSTR** contenente il valore dell'attributo da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Index* o *pAttribute* non è valido.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pAttribute* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAttributeList**](itattributelist.md)
</dt> </dl>

 

