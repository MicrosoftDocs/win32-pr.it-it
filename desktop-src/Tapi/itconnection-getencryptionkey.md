---
description: Il metodo GetEncryptionKey ottiene la chiave di crittografia.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: Metodo ITConnection::GetEncryptionKey (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a237073d4842cd26797b046a4d973390ff5ef254b574bcafbc6f10abca932aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060979"
---
# <a name="itconnectiongetencryptionkey-method"></a>Metodo ITConnection::GetEncryptionKey

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo GetEncryptionKey** ottiene la chiave di crittografia.

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

*ppKeyType* \[ Cambio\]
</dt> <dd>

Puntatore a un **BSTR** contenente il tipo di chiave di crittografia.

</dd> <dt>

*pfValidKeyData* \[ Cambio\]
</dt> <dd>

Indica la validità dei dati della chiave di crittografia.

</dd> <dt>

*ppKeyData* \[ Cambio\]
</dt> <dd>

Puntatore a un **BSTR contenente** i dati della chiave di crittografia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                                 |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppKeyType, pfValidKeyData* o *ppKeyData* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>                              |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                                               |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per i parametri *ppKeyType* *e ppKeyData.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Connessione IT**](itconnection.md)
</dt> </dl>

 

