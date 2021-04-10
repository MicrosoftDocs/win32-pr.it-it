---
description: Calcola un hash da utilizzare durante l'autenticazione del certificato.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Funzione SslComputeClientAuthHash (Sslprovider. h)
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
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227049"
---
# <a name="sslcomputeclientauthhash-function"></a>SslComputeClientAuthHash (funzione)

La funzione **SslComputeClientAuthHash** calcola un [*hash*](/windows/desktop/SecGloss/h-gly) da usare durante l'autenticazione del [*certificato*](/windows/desktop/SecGloss/c-gly) .

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*hMasterKey* \[ in\]
</dt> <dd>

Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ in\]
</dt> <dd>

Handle dell'hash dell'handshake calcolato fino a questo momento.

</dd> <dt>

*pszAlgId* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che identifica l' [*algoritmo di crittografia*](/windows/desktop/SecGloss/c-gly)richiesto. Può trattarsi di uno degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) standard o dell'identificatore di un altro algoritmo registrato.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Indirizzo di un buffer che riceve il [*BLOB della chiave*](/windows/desktop/SecGloss/k-gly). Il parametro *cbOutput* contiene la dimensione del buffer. Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **SslComputeClientAuthHash** calcola l'hash che viene inviato nel messaggio di verifica del certificato dell'handshake SSL. Il valore hash viene calcolato creando un hash che contiene il master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti. Per ulteriori informazioni sulla sequenza di handshake SSL, vedere [la descrizione dell'handshake Secure Sockets Layer (SSL)](https://support.microsoft.com/kb/257591).

Il modo in cui viene calcolato l'hash dipende dal protocollo e dal pacchetto di crittografia utilizzati. Inoltre, l'hash dipende dal tipo di chiave di autenticazione client utilizzata; il parametro *pszAlgId* indica il tipo di chiave utilizzata per l'autenticazione client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

