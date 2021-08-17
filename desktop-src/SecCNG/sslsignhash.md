---
description: Firma un hash usando la chiave privata specificata.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Funzione SslSignHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c57da628aac5c4043abe79491b90bb64d9fa3644199c96ba1e2ad93440f7c11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905620"
---
# <a name="sslsignhash-function"></a>Funzione SslSignHash

La **funzione SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) usando la chiave [*privata specificata.*](/windows/desktop/SecGloss/p-gly) Il processo di firma viene eseguito nel server.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per [*l'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*hPrivateKey* \[ Pollici\]
</dt> <dd>

Handle della chiave privata da utilizzare per firmare l'hash.

</dd> <dt>

*pbHashValue* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene l'hash da firmare.

</dd> <dt>

*cbHashValue* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbHashValue.*

</dd> <dt>

*pbSignature* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che riceve la firma dell'hash. Il *parametro cbSignature* contiene le dimensioni di questo buffer. Per determinare le dimensioni richieste del buffer, impostare il *parametro pbSignature* su **NULL.** Le dimensioni richieste del buffer verranno restituite nel *parametro pcbResult.*

</dd> <dt>

*cbSignature* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbSignature.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che, al termine, contiene il numero effettivo di byte scritti nel buffer *pbSignature.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

