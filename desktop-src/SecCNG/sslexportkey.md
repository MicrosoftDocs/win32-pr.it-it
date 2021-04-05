---
description: Restituisce una chiave di sessione SSL (Secure Sockets Layer Protocol) o una chiave temporanea pubblica in un BLOB serializzato.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Funzione SslExportKey (Sslprovider. h)
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
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967180"
---
# <a name="sslexportkey-function"></a>SslExportKey (funzione)

La funzione **SslExportKey** restituisce una [*chiave di sessione*](/windows/desktop/SecGloss/s-gly) SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) o una chiave temporanea pubblica in un [*BLOB*](/windows/desktop/SecGloss/b-gly)serializzato.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*HKEY* \[ in\]
</dt> <dd>

Handle della chiave da esportare.

Quando non si specifica una chiave, impostare questo parametro su **null**.

> [!Note]  
> Un handle *HKEY* viene ottenuto chiamando la funzione [**SslOpenPrivateKey**](sslopenprivatekey.md) . Gli handle ottenuti dalla funzione [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.

 

</dd> <dt>

*pszBlobType* \[ in\]
</dt> <dd>

Stringa Unicode con terminazione null che contiene un identificatore che specifica il tipo di BLOB da esportare. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ BLOB pubblico di BCRYPT DH \_**</dt> </dl>    | Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. Il buffer *pbOutput* riceve una [**struttura \_ \_ \_ BLOB di chiavi BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_BLOB ECCPUBLIC \_ BCRYPT**</dt> </dl>     | Esportare una chiave pubblica di [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc). Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_BLOB della \_ chiave OPACa BCRYPT \_**</dt> </dl> | Esportare una chiave simmetrica in un formato specifico per un singolo provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP). I BLOB opachi non sono trasferibili e devono essere importati utilizzando lo stesso *provider del servizio di crittografia* (CSP) che ha generato il BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_BLOB RSAPUBLIC \_ BCRYPT**</dt> </dl>     | Esportare una chiave pubblica RSA. Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB rsaKey BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un buffer che riceve il [*BLOB della chiave*](/windows/desktop/SecGloss/k-gly). Il parametro *cbOutput* contiene la dimensione del buffer. Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Indirizzo di una variabile **DWORD** che riceve il numero di byte copiati nel buffer di *pbOutput* . Se il parametro *pbOutput* è impostato su **null** quando viene chiamata la funzione, la dimensione richiesta per il buffer *pbOutput* , in byte, viene restituita nel **valore DWORD** a cui punta il parametro.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **SslExportKey** facilita il trasporto di chiavi di sessione da un processo a un altro e l'esportazione della parte pubblica di una chiave temporanea.

Quando si esportano le chiavi di sessione, il tipo di BLOB è opaco, vale a dire che il formato del BLOB è irrilevante, purché entrambe le funzioni **SslExportKey** e [**SslImportKey**](sslimportkey.md) possano interpretarlo.

Quando si esporta la parte pubblica di una chiave temporanea, il tipo di BLOB deve essere il tipo appropriato, ad esempio il BLOB **\_ pubblico NCRYPT DH \_ \_** o il **\_ \_ BLOB ECCPUBLIC NCRYPT**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

