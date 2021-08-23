---
description: Il metodo GetPhoneNumbers ottiene una matrice di numeri di telefono associati a un BLOB di conferenze.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: Metodo ITSdp::GetPhoneNumbers (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d417a86ba89269055aa7e30a94724f58da7978d58d80a61d65f6caec8793d5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060809"
---
# <a name="itsdpgetphonenumbers-method"></a>Metodo ITSdp::GetPhoneNumbers

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo GetPhoneNumbers** ottiene una matrice di numeri di telefono associati a un BLOB di conferenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumbers* \[ Cambio\]
</dt> <dd>

**Puntatore VARIANT** a SAFEARRAY di **BSTR** che elenca i numeri di telefono.

</dd> <dt>

*pNames* \[ Cambio\]
</dt> <dd>

**Puntatore VARIANT** a safeARRAY di nomi di elenco **BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                            |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pNumbers* *o pNames* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                           |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                          |



 

## <a name="remarks"></a>Commenti

Gli elenchi a *cui puntano pNumbers* e *pNames* hanno la stessa lunghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




