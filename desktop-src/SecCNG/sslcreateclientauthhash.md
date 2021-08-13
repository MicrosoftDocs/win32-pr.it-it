---
description: Recupera un handle per l'hash dell'handshake utilizzato per l'autenticazione client.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Funzione SslCreateClientAuthHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 96f1e7fa0de86439f89bf5c4c610bf5b46640533071260852c47321c5a1c6673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907088"
---
# <a name="sslcreateclientauthhash-function"></a>Funzione SslCreateClientAuthHash

La **funzione SslCreateClientAuthHash** recupera un handle per l'hash dell'handshake usato per l'autenticazione client. [](/windows/desktop/SecGloss/h-gly)

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle [*dell'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*phHandshakeHash* \[ Cambio\]
</dt> <dd>

Puntatore a una **variabile HASH \_ \_ HANDLE NCRYPT** per ricevere l'handle hash.

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifier.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pszHashAlgId* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG Algorithm Identifiers.**](cng-algorithm-identifiers.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Il *parametro hSslProvider* contiene un puntatore non valido.<br/>                |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phHandshakeHash* è impostato su **NULL.**<br/>                               |
| <dl> <dt>**NTE \_ NON \_ SUPPORTATO**</dt> <dt>0x80090029L</dt> </dl>     | La funzione selezionata non è supportata nella versione specificata dell'interfaccia.<br/> |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare buffer.<br/>                                          |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Il *parametro dwFlags* deve essere impostato su zero.<br/>                                      |



 

## <a name="remarks"></a>Commenti

La **funzione SslCreateClientAuthHash** viene chiamata per le conversazioni tls 1.2 o successive del protocollo [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) per creare oggetti hash usati per l'hashing dei messaggi di handshake. Viene chiamato una volta per ogni possibile algoritmo [*hash*](/windows/desktop/SecGloss/h-gly) che può essere usato nella firma di autenticazione client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

