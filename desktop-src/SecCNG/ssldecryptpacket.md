---
description: Decrittografa un singolo pacchetto SSL (Secure Sockets Layer Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Funzione SslDecryptPacket (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 0b058fbb01183ccf0582c0fa196bec71bfaffa2e8a44739c1ea5fb01a8148174
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906703"
---
# <a name="ssldecryptpacket-function"></a>Funzione SslDecryptPacket

la **funzione SslDecryptPacket** decrittografa un singolo [*pacchetto SECURE SOCKETS LAYER Protocol*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Handle per la chiave utilizzata per decrittografare il pacchetto.

</dd> <dt>

*pbInput* \[ Pollici\]
</dt> <dd>

Puntatore al buffer che contiene il pacchetto da decrittografare.

</dd> <dt>

*cbInput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbInput.*

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer per contenere il pacchetto decrittografato.

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Numero di byte scritti nel buffer *pbOutput.*

</dd> <dt>

*SequenceNumber* \[ Pollici\]
</dt> <dd>

Numero di sequenza corrispondente a questo pacchetto.

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



 

## <a name="remarks"></a>Commenti

La lunghezza del pacchetto può essere zero, ad esempio quando viene decrittografato un messaggio "HelloRequest".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

