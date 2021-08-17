---
description: Ottiene un handle hash utilizzato per l'hashing dei messaggi di handshake.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Funzione SslCreateHandshakeHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ea481a5b577c41eafddf9db8d80b4a3a1fe42d801bf96ed8cbc57127a4a8d91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906828"
---
# <a name="sslcreatehandshakehash-function"></a>Funzione SslCreateHandshakeHash

La **funzione SslCreateHandshakeHash** ottiene un handle hash usato per l'hashing dei messaggi di handshake.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
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

Handle hash che può essere passato ad altre funzioni del provider SSL.

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

> [!Note]  
> Questa funzione non viene usata con il protocollo SSL 2.0.

 

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifier.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare il buffer hash.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | *L'handle hSslProvider* non è valido.<br/>                   |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | *PhHandshakeHash* è Null.<br/>                            |



 

## <a name="remarks"></a>Commenti

La **funzione SslCreateHandshakeHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  La **funzione SslCreateHandshakeHash** viene chiamata per ottenere un handle hash.
2.  La [**funzione SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La [**funzione SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

