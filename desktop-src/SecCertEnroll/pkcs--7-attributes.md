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
# <a name="pkcs-7-attributes"></a>\#Attributi PKCS 7

PKCS \# 7 è uno standard di sintassi del messaggio crittografico. Un \# messaggio PKCS 7 non costituisce, da solo, una richiesta di certificato, ma può incapsulare una \# richiesta PKCS 10 o CMC in una struttura **ContentInfo** ASN. 1 utilizzando uno dei tipi di contenuto seguenti. L'incapsulamento consente di aggiungere funzionalità aggiuntive, ad esempio più firme, che non sono altrimenti disponibili.

-   **Dati**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **EncryptedData**

Gli attributi possono essere aggiunti ai campi **authenticatedAttributes** e **unauthenticatedAttributes** del tipo di contenuto **SignedData** .

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

Il processo necessario per archiviare la chiave privata di un client in un'autorità di certificazione (CA) fornisce un esempio completo di come è possibile usare gli attributi autenticati (firmati) e gli attributi non autenticati:

-   Il client crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e aggiunge i dati appropriati per il tipo di certificato richiesto.
-   Il client usa la \# richiesta PKCS 10 per inizializzare un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . La \# richiesta PKCS 10 viene inserita nella struttura **TaggedRequest** nella richiesta CMC. Per ulteriori informazioni, vedere la pagina relativa agli [attributi CMC](cmc-attributes.md).
-   Il client crittografa una chiave privata e la usa per inizializzare un oggetto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) . Il nuovo attributo **ArchiveKey** è incapsulato in una struttura **EnvelopedData** .

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

-   Il client crea un hash SHA-1 della chiave crittografata e lo usa per inizializzare un oggetto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .
-   Il client recupera la raccolta [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) dalla richiesta CMC e aggiunge gli attributi **ArchiveKey** e **ArchiveKeyHash** . Gli attributi vengono inseriti nella struttura **TaggedAttributes** della richiesta CMC.
-   Il client usa la richiesta CMC per inizializzare un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) . Questa operazione inserisce la richiesta CMC nel campo **ContentInfo** della struttura PKCS \# 7 **SignedData** .
-   L'attributo **ArchiveKeyHash** è firmato e inserito nella sequenza **AuthenticatedAttributes** della struttura **SignerInfo** .
-   L'attributo **ArchiveKey** viene inserito nella sequenza **UnauthenticatedAttributes** della struttura **SignerInfo** associata al firmatario primario del \# messaggio PKCS 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



