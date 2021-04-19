---
description: Il metodo GetEncryptionKey ottiene la chiave di crittografia.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Metodo ITConnection:: GetEncryptionKey (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326501"
---
# <a name="itconnectiongetencryptionkey-method"></a>Metodo ITConnection:: GetEncryptionKey

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetEncryptionKey** ottiene la chiave di crittografia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppKeyType* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il tipo di chiave di crittografia.

</dd> <dt>

*pfValidKeyData* \[ out\]
</dt> <dd>

Indica la validità dei dati della chiave di crittografia.

</dd> <dt>

*ppKeyData* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene i dati della chiave di crittografia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                                 |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppKeyType, pfValidKeyData* o *ppKeyData* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                              |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                                               |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per i parametri *ppKeyType* e *ppKeyData* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

