---
description: Decrittografa un singolo pacchetto di protocollo SSL (Secure Sockets Layer).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Funzione SslDecryptPacket (Sslprovider. h)
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
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967181"
---
# <a name="ssldecryptpacket-function"></a>SslDecryptPacket (funzione)

la funzione **SslDecryptPacket** decrittografa un singolo pacchetto di protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*HKEY* \[ in uscita\]
</dt> <dd>

Handle per la chiave utilizzata per decrittografare il pacchetto.

</dd> <dt>

*pbInput* \[ in\]
</dt> <dd>

Puntatore al buffer che contiene il pacchetto da decrittografare.

</dd> <dt>

*cbInput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbInput* .

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntatore a un buffer contenente il pacchetto decrittografato.

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Numero di byte scritti nel buffer *pbOutput* .

</dd> <dt>

*SequenceNumber* \[ in\]
</dt> <dd>

Numero di sequenza che corrisponde a questo pacchetto.

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

La lunghezza del pacchetto può essere zero, ad esempio quando viene decrittografato un messaggio "HelloRequest".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

