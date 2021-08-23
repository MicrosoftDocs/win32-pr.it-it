---
description: Questo argomento descrive come verificare che il sistema supporti un metodo digest.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Verificare che il sistema supporti un metodo digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272db3f7169ba66fdaa67c2943030d53e7c75927c2024750d405aa9a8246949e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600301"
---
# <a name="verify-the-system-supports-a-digest-method"></a>Verificare che il sistema supporti un metodo digest

Questo argomento descrive come verificare che il sistema supporti un metodo digest.

Le firme digitali XPS usano l'API Crypto, che fornisce metodi per verificare che il sistema supporti un metodo digest specifico. Per usare la funzione **CryptXmlEnumAlgorithmInfo** dell'API Crypto per enumerare i metodi digest supportati dal sistema, il chiamante deve fornire un metodo di callback e una struttura di dati. La **funzione CryptXmlEnumAlgorithmInfo** passa i dati di enumerazione al chiamante tramite il metodo di callback.

La struttura dei dati usata in questo esempio è illustrata nell'esempio di codice seguente e contiene i campi seguenti:

| Campo                            | Descrizione                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | Campo **LPWSTR** che punta alla stringa contenente l'URI dell'algoritmo digest da controllare. |
| **userDigestAlgorithmSupported** | Valore **booleano** che indica se l'algoritmo digest è supportato dal certificato.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



Il metodo API Crypto che enumera i metodi digest usa un metodo di callback per restituire dati al chiamante. **CryptXmlEnumAlgorithmInfo** enumera i metodi digest supportati dal sistema e chiama il metodo di callback per ogni metodo digest enumerato, fino a quando il metodo di callback non restituisce **FALSE** o finché non vengono enumerati tutti i metodi digest supportati dal sistema. Il metodo di callback in questo esempio confronta il metodo digest passato da **CryptXmlEnumAlgorithmInfo** con il metodo digest fornito dal metodo chiamante.


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



L'esempio di codice seguente esegue il wrapping della funzionalità di convalida in un singolo metodo, che restituisce un valore **booleano** che indica se il sistema supporta il metodo digest.


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Usato in questo esempio**
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

 

 
