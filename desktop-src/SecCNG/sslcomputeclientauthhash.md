---
description: Calcola un hash da usare durante l'autenticazione del certificato.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Funzione SslComputeClientAuthHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 59d1a4d8491175acb0f833cbafb430faae9b36b38a179970b7a99d6b0077591d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907162"
---
# <a name="sslcomputeclientauthhash-function"></a>Funzione SslComputeClientAuthHash

La **funzione SslComputeClientAuthHash** calcola un [*hash*](/windows/desktop/SecGloss/h-gly) da usare durante l'autenticazione [*del*](/windows/desktop/SecGloss/c-gly) certificato.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL [*(Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) Protocol).

</dd> <dt>

*hMasterKey* \[ Pollici\]
</dt> <dd>

Handle [*dell'oggetto chiave master.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*hHandshakeHash* \[ Pollici\]
</dt> <dd>

Handle dell'hash dell'handshake calcolato finora.

</dd> <dt>

*pszAlgId* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che identifica l'algoritmo [*di crittografia richiesto.*](/windows/desktop/SecGloss/c-gly) Può trattarsi di uno degli identificatori [**di algoritmo CNG**](cng-algorithm-identifiers.md) standard o dell'identificatore di un altro algoritmo registrato.

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che riceve la [*chiave BLOB*](/windows/desktop/SecGloss/k-gly). Il *parametro cbOutput* contiene le dimensioni di questo buffer. Se questo parametro è **NULL,** questa funzione inserirà le dimensioni richieste, in byte, nel **valore DWORD** a cui punta *il parametro pcbResult.*

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione SslComputeClientAuthHash** calcola l'hash inviato nel messaggio di verifica del certificato dell'handshake SSL. Il valore hash viene calcolato creando un hash che contiene il master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti. Per altre informazioni sulla sequenza di handshake SSL, vedere [Descrizione dell'handshake Secure Sockets Layer (SSL).](https://support.microsoft.com/kb/257591)

Il modo in cui viene calcolato l'hash dipende dal protocollo e dalla suite di crittografia usati. Inoltre, l'hash dipende dal tipo di chiave di autenticazione client usata. Il *parametro pszAlgId* indica il tipo di chiave usata per l'autenticazione client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

