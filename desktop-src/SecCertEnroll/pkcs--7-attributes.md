---
description: PKCS \# 7 è uno standard di sintassi del messaggio crittografico.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#Attributi PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316683"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="9d575-103">\#Attributi PKCS 7</span><span class="sxs-lookup"><span data-stu-id="9d575-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="9d575-104">PKCS \# 7 è uno standard di sintassi del messaggio crittografico.</span><span class="sxs-lookup"><span data-stu-id="9d575-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="9d575-105">Un \# messaggio PKCS 7 non costituisce, da solo, una richiesta di certificato, ma può incapsulare una \# richiesta PKCS 10 o CMC in una struttura **ContentInfo** ASN. 1 utilizzando uno dei tipi di contenuto seguenti.</span><span class="sxs-lookup"><span data-stu-id="9d575-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="9d575-106">L'incapsulamento consente di aggiungere funzionalità aggiuntive, ad esempio più firme, che non sono altrimenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="9d575-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="9d575-107">**Dati**</span><span class="sxs-lookup"><span data-stu-id="9d575-107">**Data**</span></span>
-   <span data-ttu-id="9d575-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="9d575-108">**SignedData**</span></span>
-   <span data-ttu-id="9d575-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="9d575-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="9d575-110">**SignedAndEnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="9d575-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="9d575-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="9d575-111">**DigestedData**</span></span>
-   <span data-ttu-id="9d575-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="9d575-112">**EncryptedData**</span></span>

<span data-ttu-id="9d575-113">Gli attributi possono essere aggiunti ai campi **authenticatedAttributes** e **unauthenticatedAttributes** del tipo di contenuto **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="9d575-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="9d575-114">Il processo necessario per archiviare la chiave privata di un client in un'autorità di certificazione (CA) fornisce un esempio completo di come è possibile usare gli attributi autenticati (firmati) e gli attributi non autenticati:</span><span class="sxs-lookup"><span data-stu-id="9d575-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="9d575-115">Il client crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e aggiunge i dati appropriati per il tipo di certificato richiesto.</span><span class="sxs-lookup"><span data-stu-id="9d575-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="9d575-116">Il client usa la \# richiesta PKCS 10 per inizializzare un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="9d575-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="9d575-117">La \# richiesta PKCS 10 viene inserita nella struttura **TaggedRequest** nella richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="9d575-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="9d575-118">Per ulteriori informazioni, vedere la pagina relativa agli [attributi CMC](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9d575-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="9d575-119">Il client crittografa una chiave privata e la usa per inizializzare un oggetto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) .</span><span class="sxs-lookup"><span data-stu-id="9d575-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="9d575-120">Il nuovo attributo **ArchiveKey** è incapsulato in una struttura **EnvelopedData** .</span><span class="sxs-lookup"><span data-stu-id="9d575-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   <span data-ttu-id="9d575-121">Il client crea un hash SHA-1 della chiave crittografata e lo usa per inizializzare un oggetto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .</span><span class="sxs-lookup"><span data-stu-id="9d575-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="9d575-122">Il client recupera la raccolta [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) dalla richiesta CMC e aggiunge gli attributi **ArchiveKey** e **ArchiveKeyHash** .</span><span class="sxs-lookup"><span data-stu-id="9d575-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="9d575-123">Gli attributi vengono inseriti nella struttura **TaggedAttributes** della richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="9d575-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="9d575-124">Il client usa la richiesta CMC per inizializzare un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) .</span><span class="sxs-lookup"><span data-stu-id="9d575-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="9d575-125">Questa operazione inserisce la richiesta CMC nel campo **ContentInfo** della struttura PKCS \# 7 **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="9d575-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="9d575-126">L'attributo **ArchiveKeyHash** è firmato e inserito nella sequenza **AuthenticatedAttributes** della struttura **SignerInfo** .</span><span class="sxs-lookup"><span data-stu-id="9d575-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="9d575-127">L'attributo **ArchiveKey** viene inserito nella sequenza **UnauthenticatedAttributes** della struttura **SignerInfo** associata al firmatario primario del \# messaggio PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="9d575-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d575-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d575-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d575-129">Attributi supportati</span><span class="sxs-lookup"><span data-stu-id="9d575-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



