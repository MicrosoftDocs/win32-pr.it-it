---
description: Questo argomento descrive come verificare che un certificato supporti un metodo di firma specifico.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Verificare che un certificato supporti un metodo di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098713"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Verificare che un certificato supporti un metodo di firma

Questo argomento descrive come verificare che un certificato supporti un metodo di firma specifico.

**CryptXmlEnumAlgorithmInfo** nell'API Microsoft Crypto enumera le proprietà di un certificato e viene usato in questo esempio di codice per enumerare i metodi di firma supportati dal certificato. Per usare **CryptXmlEnumAlgorithmInfo** per enumerare i metodi di firma supportati dal certificato, il chiamante deve fornire un metodo di callback e una struttura di dati nella chiamata a **CryptXmlEnumAlgorithmInfo**, consentendo al chiamante di passare dati al metodo di callback.

La struttura dei dati usata nell'esempio di codice successivo include i campi seguenti:

| Campo                               | Descrizione                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | Campo **LPWSTR** che punta alla stringa contenente l'URI dell'algoritmo di firma da controllare.                             |
| **certificateAlgorithmInfo**        | Puntatore a una **struttura CRYPT \_ OID \_ INFO** che contiene informazioni su un algoritmo di firma supportato dal certificato. |
| **userSignatureAlgorithmSupported** | Valore **booleano** che indica se l'algoritmo di firma è supportato dal certificato.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



Il metodo api Crypto che controlla il certificato usa un metodo di callback per restituire dati al chiamante. **CryptXmlEnumAlgorithmInfo** enumera i metodi di firma supportati dal certificato e chiama il metodo di callback per ogni metodo di firma finché il metodo di callback non restituisce **FALSE** o finché non vengono enumerati tutti i metodi di firma nel certificato.

Il metodo di callback nell'esempio di codice successivo cerca un metodo di firma passato da **CryptXmlEnumAlgorithmInfo** che corrisponde al metodo di firma fornito dal metodo chiamante. Quando viene trovata una corrispondenza, il metodo di callback verifica se anche il metodo di firma è supportato dal sistema. Se i metodi di firma corrispondono e sono supportati dal sistema, il metodo di firma viene contrassegnato come supportato dal sistema e il metodo di callback restituisce **FALSE.**


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



L'esempio di codice seguente esegue il wrapping della funzionalità di convalida in un unico metodo. Questo metodo restituisce un **valore booleano** che indica se il certificato supporta il metodo di firma e se il metodo di firma è supportato dal sistema.


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Usato in questo esempio**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**INFORMAZIONI \_ SULL'OID CRYPT \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[API di crittografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Errori dell'API firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori dei documenti XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
