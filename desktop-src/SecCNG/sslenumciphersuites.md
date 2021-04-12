---
description: Enumera i pacchetti di crittografia supportati da un provider del protocollo SSL (Secure Sockets Layer Protocol).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Funzione SslEnumCipherSuites (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345041"
---
# <a name="sslenumciphersuites-function"></a>SslEnumCipherSuites (funzione)

La funzione **SslEnumCipherSuites** enumera i pacchetti di crittografia supportati da un provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hPrivateKey* \[ in, facoltativo\]
</dt> <dd>

Handle di una [*chiave privata*](/windows/desktop/SecGloss/p-gly). Quando si specifica una chiave privata, **SslEnumCipherSuites** enumera i pacchetti di crittografia compatibili con la chiave privata. Ad esempio, se la chiave privata è una chiave DSS, vengono restituiti solo i pacchetti di \_ crittografia DSS dhe. Se la chiave privata è una chiave RSA, ma non supporta le operazioni di decrittografia non elaborate, i pacchetti di crittografia SSL2 non vengono restituiti.

Se non si specifica una chiave privata, impostare questo parametro su **null** .

> [!Note]  
> Un handle *hPrivateKey* viene ottenuto chiamando la funzione [**SslOpenPrivateKey**](sslopenprivatekey.md) . Gli handle ottenuti dalla funzione [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.

 

</dd> <dt>

*ppCipherSuite* \[ out\]
</dt> <dd>

Puntatore a una struttura [**del \_ \_ \_ pacchetto di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) per ricevere l'indirizzo del pacchetto di crittografia successivo nell'elenco.

</dd> <dt>

*ppEnumState* \[ in uscita\]
</dt> <dd>

Puntatore a un buffer che indica la posizione corrente nell'elenco dei pacchetti di crittografia.

Impostare il puntatore su **null** nella prima chiamata a **SslEnumCipherSuites**. Per ogni chiamata successiva, passare il valore non modificato di nuovo a **SslEnumCipherSuites**.

Quando non sono disponibili altri pacchetti di crittografia, è necessario liberare *ppEnumState* chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>      | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**Nte \_ Nessun \_ altro \_ elemento**</dt> <dt>0x8009002AL</dt> </dl> | Non sono supportati altri pacchetti di crittografia.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per enumerare tutti i pacchetti di crittografia supportati dal provider SSL, chiamare la funzione **SslEnumCipherSuites** in un ciclo fino a quando non viene restituito **\_ nessun \_ altro \_ elemento** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Ncrypt. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_pacchetto di \_ crittografia \_ SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

