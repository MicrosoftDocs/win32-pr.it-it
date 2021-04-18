---
description: Recupera un handle per l'hash di handshake utilizzato per l'autenticazione client.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Funzione SslCreateClientAuthHash (Sslprovider. h)
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
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310766"
---
# <a name="sslcreateclientauthhash-function"></a>SslCreateClientAuthHash (funzione)

La funzione **SslCreateClientAuthHash** recupera un handle per l' [*hash*](/windows/desktop/SecGloss/h-gly) di handshake usato per l'autenticazione client.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Puntatore a una variabile **dell' \_ \_ handle di hash NCRYPT** per la ricezione dell'handle hash.

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pszHashAlgId* \[ in\]
</dt> <dd>

Uno dei valori degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Il parametro *hSslProvider* contiene un puntatore non valido.<br/>                |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phHandshakeHash* è impostato su **null**.<br/>                               |
| <dl> <dt>**Nte \_ 0x80090029L non \_ supportato**</dt> <dt></dt> </dl>     | La funzione selezionata non è supportata nella versione specificata dell'interfaccia.<br/> |
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | Memoria insufficiente per allocare i buffer.<br/>                                          |
| <dl> <dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt> </dl>         | Il parametro *dwFlags* deve essere impostato su zero.<br/>                                      |



 

## <a name="remarks"></a>Commenti

La funzione **SslCreateClientAuthHash** viene chiamata per le conversazioni [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 o versioni successive per creare oggetti hash utilizzati per i messaggi di handshake hash. Viene chiamato una volta per ogni possibile [*algoritmo di hashing*](/windows/desktop/SecGloss/h-gly) che può essere usato nella firma di autenticazione client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

