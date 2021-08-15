---
description: PKCS \# 7 è uno standard di sintassi dei messaggi crittografici.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: Attributi PKCS \# 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24436a918afe2d9bd85d7c28ae330b8c022bd4e3d34d30e58aae7b9c57c4963a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774586"
---
# <a name="pkcs-7-attributes"></a>Attributi PKCS \# 7

PKCS \# 7 è uno standard di sintassi dei messaggi crittografici. Un messaggio PKCS 7 non costituisce di per sé una richiesta di certificato, ma può incapsulare una richiesta \# PKCS 10 o CMC in una \# struttura **ContentInfo** ASN.1 usando uno dei tipi di contenuto seguenti. L'incapsulamento consente di aggiungere funzionalità aggiuntive, ad esempio più firme, che non sono altrimenti disponibili.

-   **Dati**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **Encrypteddata**

Gli attributi possono essere aggiunti ai **campi authenticatedAttributes** e **unauthenticatedAttributes** del tipo di contenuto **SignedData.**

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

Il processo necessario per archiviare la chiave privata di un client in un'autorità di certificazione (CA) fornisce un esempio completo dell'uso degli attributi autenticati (firmati) e degli attributi non autenticati:

-   Il client crea un [**oggetto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e aggiunge i dati appropriati per il tipo di certificato richiesto.
-   Il client usa la richiesta PKCS \# 10 per inizializzare un [**oggetto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) La richiesta PKCS \# 10 viene inserita nella **struttura TaggedRequest** nella richiesta CMC. Per altre informazioni, vedere [Attributi CMC](cmc-attributes.md).
-   Il client crittografa una chiave privata e la usa per inizializzare un [**oggetto IX509AttributeArchiveKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) Il nuovo **attributo ArchiveKey** è incapsulato in una **struttura EnvelopedData.**

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

-   Il client crea un hash SHA-1 della chiave crittografata e lo usa per inizializzare un [**oggetto IX509AttributeArchiveKeyHash.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   Il client recupera la raccolta [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) dalla richiesta CMC e aggiunge gli attributi **ArchiveKey** e **ArchiveKeyHash.** Gli attributi vengono inseriti nella **struttura TaggedAttributes** della richiesta CMC.
-   Il client usa la richiesta CMC per inizializzare un [**oggetto IX509CertificateRequestPkcs7.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) In questo modo la richiesta CMC viene inserito **nel campo contentInfo** della struttura PKCS \# 7 **SignedData.**
-   **L'attributo ArchiveKeyHash** viene firmato e inserito nella **sequenza authenticatedAttributes** della **struttura SignerInfo.**
-   **L'attributo ArchiveKey** viene inserito nella sequenza **unauthenticatedAttributes** della struttura **SignerInfo** associata al firmatario primario del messaggio PKCS \# 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



