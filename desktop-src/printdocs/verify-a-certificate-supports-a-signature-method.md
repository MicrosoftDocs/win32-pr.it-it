---
description: In questo argomento viene descritto come verificare che un certificato supporti un metodo di firma specifico.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Verificare che un certificato supporti un metodo di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884657"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="af22f-103">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="af22f-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="af22f-104">In questo argomento viene descritto come verificare che un certificato supporti un metodo di firma specifico.</span><span class="sxs-lookup"><span data-stu-id="af22f-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="af22f-105">**CryptXmlEnumAlgorithmInfo** nell'API Microsoft Crypto enumera le proprietà di un certificato e viene usato in questo esempio di codice per enumerare i metodi di firma supportati dal certificato.</span><span class="sxs-lookup"><span data-stu-id="af22f-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="af22f-106">Per usare **CryptXmlEnumAlgorithmInfo** per enumerare i metodi di firma supportati dal certificato, il chiamante deve fornire un metodo di callback e una struttura di dati nella chiamata a **CryptXmlEnumAlgorithmInfo**, consentendo il passaggio di dati al metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="af22f-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="af22f-107">La struttura dei dati usata nell'esempio di codice successivo presenta i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="af22f-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="af22f-108">Campo</span><span class="sxs-lookup"><span data-stu-id="af22f-108">Field</span></span>                               | <span data-ttu-id="af22f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af22f-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af22f-110">**userSignatureAlgorithmToCheck**</span><span class="sxs-lookup"><span data-stu-id="af22f-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="af22f-111">Campo **LPWSTR** che punta alla stringa che contiene l'URI dell'algoritmo di firma da verificare.</span><span class="sxs-lookup"><span data-stu-id="af22f-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="af22f-112">**certificateAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="af22f-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="af22f-113">Puntatore a una struttura **di \_ \_ Informazioni OID della Crypt** che contiene informazioni su un algoritmo di firma supportato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="af22f-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="af22f-114">**userSignatureAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="af22f-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="af22f-115">Valore **booleano** che indica se l'algoritmo di firma è supportato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="af22f-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="af22f-116">Il metodo dell'API Crypto che controlla il certificato usa un metodo di callback per restituire i dati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="af22f-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="af22f-117">**CryptXmlEnumAlgorithmInfo** enumera i metodi di firma supportati dal certificato e chiama il metodo di callback per ogni metodo di firma finché il metodo di callback non restituisce **false** o finché non vengono enumerati tutti i metodi di firma del certificato.</span><span class="sxs-lookup"><span data-stu-id="af22f-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="af22f-118">Il metodo di callback nell'esempio di codice successivo Cerca un metodo di firma passato da **CryptXmlEnumAlgorithmInfo** che corrisponde al metodo di firma fornito dal metodo chiamante.</span><span class="sxs-lookup"><span data-stu-id="af22f-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="af22f-119">Quando viene trovata una corrispondenza, il metodo di callback controlla se il metodo di firma è supportato anche dal sistema.</span><span class="sxs-lookup"><span data-stu-id="af22f-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="af22f-120">Se i metodi di firma corrispondono e sono supportati dal sistema, il metodo di firma è contrassegnato come supportato dal sistema e il metodo di callback restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="af22f-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


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



<span data-ttu-id="af22f-121">Nell'esempio di codice seguente viene eseguito il wrapping della funzionalità di convalida in un singolo metodo.</span><span class="sxs-lookup"><span data-stu-id="af22f-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="af22f-122">Questo metodo restituisce un valore **booleano** che indica se il certificato supporta il metodo di firma e se il metodo di firma è supportato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="af22f-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af22f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af22f-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="af22f-124">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="af22f-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="af22f-125">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="af22f-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="af22f-126">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="af22f-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="af22f-127">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="af22f-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="af22f-128">**Usato in questo esempio**</span><span class="sxs-lookup"><span data-stu-id="af22f-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="af22f-129">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="af22f-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="af22f-130">**\_informazioni Oid \_ crypt**</span><span class="sxs-lookup"><span data-stu-id="af22f-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="af22f-131">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="af22f-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="af22f-132">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="af22f-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="af22f-133">API di crittografia</span><span class="sxs-lookup"><span data-stu-id="af22f-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="af22f-134">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="af22f-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="af22f-135">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="af22f-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="af22f-136">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="af22f-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="af22f-137">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="af22f-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
