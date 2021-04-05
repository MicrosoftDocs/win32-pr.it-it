---
description: Restituisce un handle per l'hash di handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Funzione SslHashHandshake (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968221"
---
# <a name="sslhashhandshake-function"></a>SslHashHandshake (funzione)

La funzione **SslHashHandshake** restituisce un handle per l'hash di handshake.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*hHandshakeHash* \[ in uscita\]
</dt> <dd>

Handle per l'oggetto hash.

</dd> <dt>

*pbInput* \[ out\]
</dt> <dd>

Indirizzo di un buffer che contiene i dati di cui eseguire l'hashing.

</dd> <dt>

*cbInput* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbInput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

## <a name="remarks"></a>Commenti

La funzione **SslHashHandshake** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  Viene chiamata la funzione [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) per ottenere un handle hash.
2.  La funzione **SslHashHandshake** viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La funzione [**SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

