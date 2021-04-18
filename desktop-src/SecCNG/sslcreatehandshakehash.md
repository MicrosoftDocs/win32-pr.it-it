---
description: Ottiene un handle hash utilizzato per l'hashing dei messaggi di handshake.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Funzione SslCreateHandshakeHash (Sslprovider. h)
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
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310764"
---
# <a name="sslcreatehandshakehash-function"></a>SslCreateHandshakeHash (funzione)

La funzione **SslCreateHandshakeHash** ottiene un handle hash utilizzato per l'hashing dei messaggi di handshake.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Handle hash che può essere passato ad altre funzioni del provider SSL.

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

> [!Note]  
> Questa funzione non viene utilizzata con il protocollo SSL 2,0.

 

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | Memoria insufficiente per l'allocazione del buffer hash.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle *hSslProvider* non valido.<br/>                   |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | *PhHandshakeHash* è null.<br/>                            |



 

## <a name="remarks"></a>Commenti

La funzione **SslCreateHandshakeHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  Viene chiamata la funzione **SslCreateHandshakeHash** per ottenere un handle hash.
2.  La funzione [**SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La funzione [**SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

