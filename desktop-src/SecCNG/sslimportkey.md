---
description: Importa una chiave nel provider Secure Sockets Layer protocol (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Funzione SslImportKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 00dbe668c28e234c0ed4fdc7950b6b9627ae5aaba46bbef4e17d1eb8cb213f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906089"
---
# <a name="sslimportkey-function"></a>Funzione SslImportKey

La **funzione SslImportKey** importa una chiave nel provider [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*phKey* \[ Cambio\]
</dt> <dd>

Puntatore all'handle della chiave [*crittografica*](/windows/desktop/SecGloss/c-gly) per ricevere la chiave importata.

</dd> <dt>

*pszBlobType* \[ Pollici\]
</dt> <dd>

Stringa Unicode con terminazione Null contenente un identificatore che specifica il tipo di [*BLOB*](/windows/desktop/SecGloss/b-gly) contenuto nel buffer *pbInput.* Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**BLOB \_ PUBBLICO BCRYPT DH \_ \_**</dt> </dl>    | Esportare una Diffie-Hellman [*pubblica*](/windows/desktop/SecGloss/p-gly). Il *buffer pbOutput* riceve una struttura [**BLOB \_ BCRYPT DH \_ KEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt> </dl>     | Esportare una chiave pubblica ECC [](/windows/desktop/SecGloss/p-gly) [*(elliptic Curve Cryptography).*](/windows/desktop/SecGloss/e-gly) Il *buffer pbOutput* riceve una struttura [**BLOB \_ ECCKEY \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BLOB DI \_ CHIAVI OPAQUE BCRYPT \_ \_**</dt> </dl> | Esportare [*una chiave simmetrica*](/windows/desktop/SecGloss/s-gly) in un formato specifico per un singolo provider del [*servizio di*](/windows/desktop/SecGloss/c-gly) crittografia (CSP). I BLOB opachi non sono trasferibili e devono essere importati usando lo stesso provider di servizi di archiviazione che ha generato il BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt> </dl>     | Esportare una [*chiave pubblica RSA.*](/windows/desktop/SecGloss/r-gly) Il *buffer pbOutput* riceve una struttura [**BLOB \_ RSAKEY \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ Pollici\]
</dt> <dd>

Puntatore al buffer che contiene il [*BLOB della chiave.*](/windows/desktop/SecGloss/k-gly)

</dd> <dt>

*cbKeyBlob* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbKeyBlob.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | *L'handle hSslProvider* non è valido.<br/>                       |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phKey* è **NULL.**<br/>                            |



 

## <a name="remarks"></a>Commenti

È possibile usare la **funzione SslImportKey** per importare le chiavi di sessione come parte del processo di trasferimento delle chiavi di sessione da un processo a un altro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

