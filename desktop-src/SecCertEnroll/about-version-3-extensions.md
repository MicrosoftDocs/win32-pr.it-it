---
description: I certificati X.509 versione 3 contengono i campi di base definiti nelle versioni 1 e 2 più le estensioni di certificato. Nell'esempio seguente viene illustrata la sintassi ASN. 1 delle estensioni del certificato.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Estensioni versione 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231503"
---
# <a name="version-3-extensions"></a><span data-ttu-id="8a2f3-104">Estensioni versione 3</span><span class="sxs-lookup"><span data-stu-id="8a2f3-104">Version 3 Extensions</span></span>

<span data-ttu-id="8a2f3-105">I certificati X.509 versione 3 contengono i campi di base definiti nelle versioni 1 e 2 più le estensioni di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="8a2f3-106">Nell'esempio seguente viene illustrata la sintassi ASN. 1 delle estensioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="8a2f3-107">Nella tabella seguente sono elencate le estensioni standard della versione 3 e i relativi identificatori di oggetto (OID).</span><span class="sxs-lookup"><span data-stu-id="8a2f3-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="8a2f3-108">Microsoft supporta questi e include estensioni personalizzate aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="8a2f3-109">Per ulteriori informazioni, vedere [estensioni](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8a2f3-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="8a2f3-110">Estensione</span><span class="sxs-lookup"><span data-stu-id="8a2f3-110">Extension</span></span>                                         | <span data-ttu-id="8a2f3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a2f3-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2f3-112">Identificatore di chiave dell'autorità (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="8a2f3-113">Identifica la chiave pubblica dell'autorità di certificazione corrispondente alla chiave privata dell'autorità usata per firmare il certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="8a2f3-114">Vincoli di base (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="8a2f3-115">Specifica se l'entità può essere usata come autorità di certificazione e, in caso affermativo, il numero di autorità di certificazione subordinate che possono esistere nella catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="8a2f3-116">Criteri certificati (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="8a2f3-117">Specifica i criteri in base ai quali il certificato è stato rilasciato e gli scopi per cui può essere usato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="8a2f3-118">Punti di distribuzione CRL (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="8a2f3-119">Contiene l'URI dell'elenco di [*revoche di certificati*](/windows/desktop/SecGloss/c-gly) (CRL) di base.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="8a2f3-120">Utilizzo chiavi avanzato (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="8a2f3-121">Specifica il modo in cui è possibile usare la chiave pubblica contenuta nel certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="8a2f3-122">Nome alternativo autorità emittente (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="8a2f3-123">Specifica una o più forme di denominazione alternative per l'autorità di certificazione della richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="8a2f3-124">Utilizzo chiave (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="8a2f3-125">Specifica le restrizioni relative alle operazioni eseguibili dalla chiave pubblica contenuta nel certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="8a2f3-126">Vincoli di nome (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="8a2f3-127">Specifica lo spazio dei nomi all'interno del quale devono trovarsi tutti i nomi del soggetto in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="8a2f3-128">L'estensione è usata solo in un certificato di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="8a2f3-129">Vincoli dei criteri (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="8a2f3-130">Vincola la convalida del percorso vietando il mapping dei criteri o richiedendo che ogni certificato nella gerarchia contenga un identificatore di criteri accettabile.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="8a2f3-131">L'estensione è usata solo in un certificato di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="8a2f3-132">Mapping dei criteri (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="8a2f3-133">Specifica i criteri in un'autorità di certificazione subordinata corrispondenti ai criteri dell'autorità di certificazione emittente.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="8a2f3-134">Periodo di utilizzo chiave privata (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="8a2f3-135">Specifica un periodo di validità per la chiave privata diverso da quello del certificato a cui la chiave è associata.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="8a2f3-136">Nome alternativo del soggetto (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="8a2f3-137">Specifica una o più forme di denominazione alternative per il soggetto della richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="8a2f3-138">Esempi di forme alternative includono indirizzi email, nomi DNS; indirizzi IP e URI.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="8a2f3-139">Attributi di directory soggetto (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="8a2f3-140">Trasmette gli attributi di identificazione, ad esempio la nazionalità, del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="8a2f3-141">Il valore dell'estensione è una sequenza di coppie di valori OID.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="8a2f3-142">Identificatore di chiave del soggetto (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="8a2f3-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="8a2f3-143">Distingue tra più chiavi pubbliche detenute dal soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="8a2f3-144">Il valore dell'estensione è in genere un hash SHA-1 della chiave.</span><span class="sxs-lookup"><span data-stu-id="8a2f3-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="8a2f3-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a2f3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a2f3-146">Campi di base</span><span class="sxs-lookup"><span data-stu-id="8a2f3-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="8a2f3-147">Campi versione 2</span><span class="sxs-lookup"><span data-stu-id="8a2f3-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="8a2f3-148">Certificati di chiave pubblica X. 509</span><span class="sxs-lookup"><span data-stu-id="8a2f3-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

