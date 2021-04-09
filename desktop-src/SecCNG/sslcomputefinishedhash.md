---
description: Calcola l'hash inviato nel messaggio terminato dell'handshake del protocollo di Secure Sockets Layer (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Funzione SslComputeFinishedHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967185"
---
# <a name="sslcomputefinishedhash-function"></a>SslComputeFinishedHash (funzione)

La funzione **SslComputeFinishedHash** calcola l' [*hash*](/windows/desktop/SecGloss/h-gly) inviato nel messaggio finito dell'handshake SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ). Per ulteriori informazioni sulla sequenza di handshake SSL, vedere [la descrizione dell'handshake Secure Sockets Layer (SSL)](https://support.microsoft.com/kb/257591).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hMasterKey* \[ in\]
</dt> <dd>

Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ in\]
</dt> <dd>

Handle dell'hash dei messaggi di handshake.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve l'hash per il messaggio di fine.

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Una delle seguenti costanti.



| Valore                                                                                                                                                                                                                                                      | Significato                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Flag client SSL**</dt> <dt>0x00000001</dt> </dl> | Specifica che si tratta di una chiamata client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Flag server SSL**</dt> <dt>0x00000002</dt> </dl> | Specifica che si tratta di una chiamata al server.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Handle non valido**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **SslComputeFinishedHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  Viene chiamata la funzione [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) per ottenere un handle hash.
2.  La funzione [**SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La funzione **SslComputeFinishedHash** viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

Il valore hash viene calcolato eseguendo l'hashing della master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti.

Il valore di *cbOutput* determina la lunghezza dei dati hash. Quando si usa il protocollo TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,0, deve essere sempre 12 (byte). Per ulteriori informazioni, vedere [la versione 1,0 del protocollo TLS](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

