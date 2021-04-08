---
description: In questo argomento viene descritto come verificare che il sistema supporti un metodo digest.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Verificare che il sistema supporti un metodo digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884658"
---
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="adb70-103">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="adb70-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="adb70-104">In questo argomento viene descritto come verificare che il sistema supporti un metodo digest.</span><span class="sxs-lookup"><span data-stu-id="adb70-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="adb70-105">Le firme digitali XPS usano l'API Crypto, che fornisce i metodi per verificare che il sistema supporti un metodo digest specifico.</span><span class="sxs-lookup"><span data-stu-id="adb70-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="adb70-106">Per usare la funzione **CryptXmlEnumAlgorithmInfo** dell'API Crypto per enumerare i metodi digest supportati dal sistema, il chiamante deve fornire un metodo di callback e una struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="adb70-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="adb70-107">La funzione **CryptXmlEnumAlgorithmInfo** passa nuovamente i dati di enumerazione al chiamante tramite il metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="adb70-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="adb70-108">La struttura dei dati usata in questo esempio è illustrata nell'esempio di codice seguente e contiene i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="adb70-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="adb70-109">Campo</span><span class="sxs-lookup"><span data-stu-id="adb70-109">Field</span></span>                            | <span data-ttu-id="adb70-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adb70-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb70-111">**userDigestAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="adb70-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="adb70-112">Campo **LPWSTR** che punta alla stringa che contiene l'URI dell'algoritmo digest da verificare.</span><span class="sxs-lookup"><span data-stu-id="adb70-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="adb70-113">**userDigestAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="adb70-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="adb70-114">Valore **booleano** che indica se l'algoritmo digest è supportato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="adb70-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="adb70-115">Il metodo dell'API Crypto che enumera i metodi digest usa un metodo di callback per restituire dati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="adb70-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="adb70-116">**CryptXmlEnumAlgorithmInfo** enumera i metodi digest supportati dal sistema e chiama il metodo di callback per ogni metodo digest enumerato, finché il metodo di callback non restituisce **false** o finché non vengono enumerati tutti i metodi digest supportati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="adb70-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="adb70-117">Il metodo di callback in questo esempio confronta il metodo digest passato da **CryptXmlEnumAlgorithmInfo** con il metodo digest fornito dal metodo chiamante.</span><span class="sxs-lookup"><span data-stu-id="adb70-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


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



<span data-ttu-id="adb70-118">Nell'esempio di codice seguente viene eseguito il wrapping della funzionalità di convalida in un singolo metodo, che restituisce un valore **booleano** che indica se il sistema supporta il metodo digest.</span><span class="sxs-lookup"><span data-stu-id="adb70-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="adb70-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="adb70-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="adb70-120">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="adb70-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="adb70-121">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="adb70-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="adb70-122">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="adb70-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="adb70-123">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="adb70-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="adb70-124">**Usato in questo esempio**</span><span class="sxs-lookup"><span data-stu-id="adb70-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="adb70-125">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="adb70-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="adb70-126">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="adb70-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="adb70-127">API di crittografia</span><span class="sxs-lookup"><span data-stu-id="adb70-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="adb70-128">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="adb70-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="adb70-129">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="adb70-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="adb70-130">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="adb70-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="adb70-131">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="adb70-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
