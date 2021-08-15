---
description: Enumera i pacchetti di crittografia supportati da un provider Secure Sockets Layer protocol (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Funzione SslEnumCipherSuites (Sslprovider.h)
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
ms.openlocfilehash: 7d9fb40bf6bfebff6d0659640dfb68b718586ac822c8a779a56de300b8d55b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906693"
---
# <a name="sslenumciphersuites-function"></a>Funzione SslEnumCipherSuites

La **funzione SslEnumCipherSuites** enumera i pacchetti di crittografia supportati da un provider Secure Sockets Layer [*protocol*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hPrivateKey* \[ in, facoltativo\]
</dt> <dd>

Handle di una [*chiave privata.*](/windows/desktop/SecGloss/p-gly) Quando viene specificata una chiave privata, **SslEnumCipherSuites** enumera i pacchetti di crittografia compatibili con la chiave privata. Ad esempio, se la chiave privata è una chiave DSS, vengono restituite solo le suite di crittografia \_ DSS DHE. Se la chiave privata è una chiave RSA, ma non supporta operazioni di decrittografia non elaborata, i pacchetti di crittografia SSL2 non vengono restituiti.

Impostare questo parametro su **NULL** quando non si specifica una chiave privata.

> [!Note]  
> Un *handle hPrivateKey* viene ottenuto chiamando la [**funzione SslOpenPrivateKey.**](sslopenprivatekey.md) Gli handle ottenuti dalla [**funzione NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.

 

</dd> <dt>

*ppCipherSuite* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura \_ \_ CIPHER \_ SUITE SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) per ricevere l'indirizzo della suite di crittografia successiva nell'elenco.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Puntatore a un buffer che indica la posizione corrente nell'elenco di suite di crittografia.

Impostare il **puntatore su NULL** alla prima chiamata a **SslEnumCipherSuites**. A ogni chiamata successiva, passare nuovamente il valore non modificato a **SslEnumCipherSuites**.

Quando non sono disponibili altri pacchetti di crittografia, è necessario liberare *ppEnumState* chiamando la [**funzione SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>      | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**NTE \_ NO \_ MORE \_ ITEMS**</dt> <dt>0x8009002AL</dt> </dl> | Non sono supportate altre suite di crittografia.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per enumerare tutti i pacchetti di crittografia supportati dal provider SSL, chiamare la funzione **SslEnumCipherSuites** in un ciclo fino a quando non viene restituito **NTE \_ NO MORE \_ \_ ITEMS.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Ncrypt.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCRYPT \_ SSL \_ CIPHER \_ SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

