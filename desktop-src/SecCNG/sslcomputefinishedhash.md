---
description: Calcola l'hash inviato nel messaggio completato dell'handshake Secure Sockets Layer protocol (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Funzione SslComputeFinishedHash (Sslprovider.h)
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
ms.openlocfilehash: e0f23a58111bfcebbe668cd3b6c50a135da0dae240907f09a65d60ef1cebdda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907142"
---
# <a name="sslcomputefinishedhash-function"></a>Funzione SslComputeFinishedHash

La **funzione SslComputeFinishedHash** calcola l'hash inviato nel messaggio completato dell'handshake [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL). [](/windows/desktop/SecGloss/h-gly) Per altre informazioni sulla sequenza di handshake SSL, vedere [Descrizione dell'handshake Secure Sockets Layer (SSL).](https://support.microsoft.com/kb/257591)

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hMasterKey* \[ Pollici\]
</dt> <dd>

Handle [*dell'oggetto chiave*](/windows/desktop/SecGloss/m-gly) master.

</dd> <dt>

*hHandshakeHash* \[ Pollici\]
</dt> <dd>

Handle dell'hash dei messaggi di handshake.

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve l'hash per il messaggio di fine.

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Una delle costanti seguenti.



| Valore                                                                                                                                                                                                                                                      | Significato                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ Flag \_ \_ CLIENT SSL**</dt> <dt>0x00000001</dt> </dl> | Specifica che si tratta di una chiamata client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ FLAG \_ \_ DEL SERVER SSL**</dt> <dt>0x00000002</dt> </dl> | Specifica che si tratta di una chiamata al server.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ 2148073510**</dt> <dt>(0x80090026)</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione SslComputeFinishedHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.

1.  La [**funzione SslCreateHandshakeHash**](sslcreatehandshakehash.md) viene chiamata per ottenere un handle hash.
2.  La [**funzione SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.
3.  La **funzione SslComputeFinishedHash** viene chiamata con l'handle hash per ottenere il digest dei dati con hash.

Il valore hash viene calcolato tramite hash del master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti.

Il valore *di cbOutput* determina la lunghezza dei dati hash. Quando viene [*Transport Layer Security protocollo*](/windows/desktop/SecGloss/t-gly) TLS (Tls) 1.0, deve essere sempre 12 (byte). Per altre informazioni, vedere [Protocollo TLS versione 1.0.](https://www.ietf.org/rfc/rfc2246.txt)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

