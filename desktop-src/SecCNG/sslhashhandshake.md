---
description: Restituisce un handle per l'hash dell'handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Funzione SslHashHandshake (Sslprovider.h)
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
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906099"
---
# <a name="sslhashhandshake-function"></a>Funzione SslHashHandshake

La **funzione SslHashHandshake** restituisce un handle per l'hash dell'handshake.

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per [*l'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

Handle per l'oggetto hash.

</dd> <dt>

*pbInput* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che contiene i dati di cui eseguire l'hashing.

</dd> <dt>

*cbInput* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbInput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

## <a name="remarks"></a>Commenti

La **funzione SslHashHandshake** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  La [**funzione SslCreateHandshakeHash**](sslcreatehandshakehash.md) viene chiamata per ottenere un handle hash.
2.  La **funzione SslHashHandshake** viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La [**funzione SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

