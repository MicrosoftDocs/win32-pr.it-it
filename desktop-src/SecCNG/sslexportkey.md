---
description: Restituisce una Secure Sockets Layer di sessione SSL (Secure Sockets Layer Protocol) o una chiave effimera pubblica in un BLOB serializzato.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Funzione SslExportKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 073e922ce8c1a79e81d991c869743148b5a581503192a10dfb9cd6e64707d83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906673"
---
# <a name="sslexportkey-function"></a>Funzione SslExportKey

La **funzione SslExportKey** restituisce una chiave Secure Sockets Layer [](/windows/desktop/SecGloss/s-gly) di sessione SSL (Secure Sockets Layer [*Protocol)*](/windows/desktop/SecGloss/s-gly) o una chiave effimera pubblica in un BLOB [*serializzato.*](/windows/desktop/SecGloss/b-gly)

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hKey* \[ Pollici\]
</dt> <dd>

Handle della chiave da esportare.

Quando non si specifica una chiave, impostare questo parametro su **NULL.**

> [!Note]  
> Un handle *hKey* viene ottenuto chiamando la [**funzione SslOpenPrivateKey.**](sslopenprivatekey.md) Gli handle ottenuti dalla [**funzione NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.

 

</dd> <dt>

*pszBlobType* \[ Pollici\]
</dt> <dd>

Stringa Unicode con terminazione Null contenente un identificatore che specifica il tipo di BLOB da esportare. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**BLOB \_ PUBBLICO BCRYPT DH \_ \_**</dt> </dl>    | Esportare una Diffie-Hellman [*pubblica.*](/windows/desktop/SecGloss/p-gly) Il *buffer pbOutput* riceve una struttura BLOB della chiave [**\_ DH \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt> </dl>     | Esportare [*una chiave pubblica ECC (elliptic curve cryptography).*](/windows/desktop/SecGloss/e-gly) Il *buffer pbOutput* riceve una [**struttura BLOB \_ ECCKEY \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BLOB DI \_ CHIAVI OPACHE BCRYPT \_ \_**</dt> </dl> | Esportare una chiave simmetrica in un formato specifico di un singolo provider del [*servizio di*](/windows/desktop/SecGloss/c-gly) crittografia (CSP). I BLOB opachi non sono trasferibili e devono essere importati usando lo stesso *provider* del servizio di crittografia (CSP) che ha generato il BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt> </dl>     | Esportare una chiave pubblica RSA. Il *buffer pbOutput* riceve una [**struttura BLOB BCRYPT \_ RSAKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un buffer che riceve la [*chiave BLOB*](/windows/desktop/SecGloss/k-gly). Il *parametro cbOutput* contiene le dimensioni di questo buffer. Se questo parametro è **NULL,** questa funzione inserirà le dimensioni richieste, in byte, nel **valore DWORD** a cui punta *il parametro pcbResult.*

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Indirizzo di una **variabile DWORD** che riceve il numero di byte copiati nel buffer *pbOutput.* Se il *parametro pbOutput* è impostato su **NULL** quando viene chiamata la funzione, le dimensioni richieste per il buffer *pbOutput,* in byte, vengono restituite nel **valore DWORD** a cui punta questo parametro.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione SslExportKey** facilita il trasporto delle chiavi di sessione da un processo a un altro, nonché l'esportazione della parte pubblica come chiave effimera.

Quando si esportano chiavi di sessione, il tipo DI BLOB è opaco, vale a dire che il formato del BLOB è irrilevante, purché entrambe le funzioni **SslExportKey** e [**SslImportKey**](sslimportkey.md) possano interpretarlo.

Quando si esporta la parte pubblica di una chiave effimera, il tipo BLOB deve essere il tipo appropriato, ad esempio **NCRYPT \_ DH \_ PUBLIC \_ BLOB** o **NCRYPT \_ ECCPUBLIC \_ BLOB.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

