---
description: Firma un hash usando la chiave privata specificata.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Funzione SslSignHash (Sslprovider. h)
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
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484628"
---
# <a name="sslsignhash-function"></a>SslSignHash (funzione)

La funzione **SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) usando la [*chiave privata*](/windows/desktop/SecGloss/p-gly)specificata. Il processo di firma viene eseguito sul server.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*hPrivateKey* \[ in\]
</dt> <dd>

Handle per la chiave privata da utilizzare per firmare l'hash.

</dd> <dt>

*pbHashValue* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente l'hash da firmare.

</dd> <dt>

*cbHashValue* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ out\]
</dt> <dd>

Indirizzo di un buffer che riceve la firma dell'hash. Il parametro *cbSignature* contiene la dimensione del buffer. Per determinare le dimensioni di dimensioni richieste del buffer, impostare il parametro *pbSignature* su **null**. La dimensione richiesta del buffer verrà restituita nel parametro *pcbResult* .

</dd> <dt>

*cbSignature* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbSignature* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Puntatore a un valore che, al termine, contiene il numero effettivo di byte scritti nel buffer *pbSignature* .

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



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

