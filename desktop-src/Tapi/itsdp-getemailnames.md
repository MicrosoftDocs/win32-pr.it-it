---
description: Il metodo GetEmailNames ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: Metodo ITSdp::GetEmailNames (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140264"
---
# <a name="itsdpgetemailnames-method"></a>Metodo ITSdp::GetEmailNames

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo GetEmailNames** ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAddresses* \[ Cambio\]
</dt> <dd>

**Puntatore VARIANT** a SAFEARRAY di **BSTR** che elenca gli indirizzi di posta elettronica.

</dd> <dt>

*pNames* \[ Cambio\]
</dt> <dd>

**Puntatore VARIANT** a safeARRAY di nomi di elenco **BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pAddresses* *o pNames* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>           |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                            |



 

## <a name="remarks"></a>Commenti

Gli elenchi a *cui puntano pAddresses* e *pNames* hanno la stessa lunghezza.

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

 

 




