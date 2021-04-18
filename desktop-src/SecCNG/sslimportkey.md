---
description: Importa una chiave nel provider del protocollo SSL (Secure Sockets Layer Protocol).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Funzione SslImportKey (Sslprovider. h)
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
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310761"
---
# <a name="sslimportkey-function"></a>SslImportKey (funzione)

La funzione **SslImportKey** importa una chiave nel provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Puntatore all'handle della [*chiave crittografica*](/windows/desktop/SecGloss/c-gly) per la ricezione della chiave importata.

</dd> <dt>

*pszBlobType* \[ in\]
</dt> <dd>

Stringa Unicode con terminazione null che contiene un identificatore che specifica il tipo di [*BLOB*](/windows/desktop/SecGloss/b-gly) contenuto nel buffer *pbInput* . Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ BLOB pubblico di BCRYPT DH \_**</dt> </dl>    | Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. Il buffer *pbOutput* riceve una [**struttura \_ \_ \_ BLOB di chiavi BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_BLOB ECCPUBLIC \_ BCRYPT**</dt> </dl>     | Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)di [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc). Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_BLOB della \_ chiave OPACa BCRYPT \_**</dt> </dl> | Esportare una [*chiave simmetrica*](/windows/desktop/SecGloss/s-gly) in un formato specifico per un singolo provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP). I BLOB opachi non sono trasferibili e devono essere importati utilizzando lo stesso CSP che ha generato il BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_BLOB RSAPUBLIC \_ BCRYPT**</dt> </dl>     | Esportare una chiave pubblica [*RSA*](/windows/desktop/SecGloss/r-gly) . Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB rsaKey BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ in\]
</dt> <dd>

Puntatore al buffer che contiene il BLOB della [*chiave*](/windows/desktop/SecGloss/k-gly).

</dd> <dt>

*cbKeyBlob* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbKeyBlob* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle *hSslProvider* non valido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phKey* è **null**.<br/>                            |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare la funzione **SslImportKey** per importare le chiavi della sessione come parte del processo di trasferimento delle chiavi di sessione da un processo a un altro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

