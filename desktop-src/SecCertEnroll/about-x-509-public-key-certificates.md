---
description: La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificati di chiave pubblica X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569591"
---
# <a name="x509-public-key-certificates"></a><span data-ttu-id="7345d-103">Certificati di chiave pubblica X. 509</span><span class="sxs-lookup"><span data-stu-id="7345d-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="7345d-104">La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="7345d-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="7345d-105">Le chiavi sono correlate matematicamente e il contenuto crittografato tramite una delle chiavi può essere decrittografato solo utilizzando l'altro.</span><span class="sxs-lookup"><span data-stu-id="7345d-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="7345d-106">La chiave privata viene mantenuta segreta.</span><span class="sxs-lookup"><span data-stu-id="7345d-106">The private key is kept secret.</span></span> <span data-ttu-id="7345d-107">La chiave pubblica in genere è incorporata in un certificato binario e il certificato viene pubblicato in un database che può essere raggiunto da tutti gli utenti autorizzati.</span><span class="sxs-lookup"><span data-stu-id="7345d-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="7345d-108">Lo standard di infrastruttura a chiave pubblica (PKI) X. 509 identifica i requisiti per i certificati di chiave pubblica affidabili.</span><span class="sxs-lookup"><span data-stu-id="7345d-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="7345d-109">Un certificato è una struttura di dati firmati che associa una chiave pubblica a una persona, un computer o un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7345d-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="7345d-110">I certificati vengono rilasciati da [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CAS).</span><span class="sxs-lookup"><span data-stu-id="7345d-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="7345d-111">Tutti gli utenti che fanno parte di proteggere le comunicazioni che usano una chiave pubblica si affidano alla CA per verificare adeguatamente le identità dei singoli, dei sistemi o delle entità a cui rilascia i certificati.</span><span class="sxs-lookup"><span data-stu-id="7345d-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="7345d-112">Il livello di verifica dipende in genere dal livello di sicurezza richiesto per la transazione.</span><span class="sxs-lookup"><span data-stu-id="7345d-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="7345d-113">Se la CA può verificare adeguatamente l'identità del richiedente, firma (crittografa), codifica e rilascia il certificato.</span><span class="sxs-lookup"><span data-stu-id="7345d-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="7345d-114">Un certificato è una struttura di dati firmati che associa una chiave pubblica a un'entità.</span><span class="sxs-lookup"><span data-stu-id="7345d-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="7345d-115">Nell'esempio seguente viene illustrata la sintassi [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) per il certificato [*X. 509*](/windows/desktop/SecGloss/x-gly) della versione 3.</span><span class="sxs-lookup"><span data-stu-id="7345d-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

<span data-ttu-id="7345d-116">Dall'inizio della 1998 sono state sviluppate tre versioni dello standard del certificato di chiave pubblica X. 509.</span><span class="sxs-lookup"><span data-stu-id="7345d-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="7345d-117">Come illustrato nella figura seguente, ogni versione successiva della struttura di dati ha mantenuto i campi esistenti nelle versioni precedenti e ne ha aggiunto altri.</span><span class="sxs-lookup"><span data-stu-id="7345d-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![certificati x. 509 versioni 1, 2 e 3](images/x509certificateversions.png)

<span data-ttu-id="7345d-119">Gli argomenti seguenti illustrano i campi disponibili in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="7345d-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="7345d-120">Campi di base</span><span class="sxs-lookup"><span data-stu-id="7345d-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="7345d-121">Campi versione 2</span><span class="sxs-lookup"><span data-stu-id="7345d-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="7345d-122">Estensioni versione 3</span><span class="sxs-lookup"><span data-stu-id="7345d-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="7345d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7345d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7345d-124">Infrastruttura a chiave pubblica (PKI)</span><span class="sxs-lookup"><span data-stu-id="7345d-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 
