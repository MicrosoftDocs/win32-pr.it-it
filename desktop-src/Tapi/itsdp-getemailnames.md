---
description: Il metodo GetEmailNames ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Metodo ITSdp:: GetEmailNames (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324761"
---
# <a name="itsdpgetemailnames-method"></a>Metodo ITSdp:: GetEmailNames

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetEmailNames** ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAddresses* \[ out\]
</dt> <dd>

Puntatore **Variant** a un SAFEARRAY di **BSTR** s che elenca indirizzi di posta elettronica.

</dd> <dt>

*pNames* \[ out\]
</dt> <dd>

Puntatore **Variant** a un SAFEARRAY di nomi di elenco di **BSTR**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pAddresses* o *pNames* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>           |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                            |



 

## <a name="remarks"></a>Commenti

Gli elenchi a cui *pAddresses* e *pNames* puntano sono della stessa lunghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




