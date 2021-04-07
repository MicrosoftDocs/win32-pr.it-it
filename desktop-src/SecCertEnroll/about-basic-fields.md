---
description: Un certificato X. 509 versione 1 contiene i campi seguenti. I campi della versione 2 sono illustrati nei campi della versione 2. I campi della versione 3 sono illustrati nelle estensioni della versione 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881681"
---
# <a name="basic-fields"></a><span data-ttu-id="afa2a-105">Campi di base</span><span class="sxs-lookup"><span data-stu-id="afa2a-105">Basic Fields</span></span>

<span data-ttu-id="afa2a-106">Un certificato X. 509 versione 1 contiene i campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="afa2a-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="afa2a-107">I campi della versione 2 sono illustrati nei [campi della versione 2](about-version-2-fields.md).</span><span class="sxs-lookup"><span data-stu-id="afa2a-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="afa2a-108">I campi della versione 3 sono illustrati nelle [estensioni della versione 3](about-version-3-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="afa2a-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="afa2a-109">Versione</span><span class="sxs-lookup"><span data-stu-id="afa2a-109">Version</span></span>

<span data-ttu-id="afa2a-110">Specifica il numero di versione del certificato codificato.</span><span class="sxs-lookup"><span data-stu-id="afa2a-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="afa2a-111">Attualmente, i valori possibili di questo campo sono 0, 1 o 2, ma questo può essere espanso in futuro.</span><span class="sxs-lookup"><span data-stu-id="afa2a-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="afa2a-112">Numero di serie</span><span class="sxs-lookup"><span data-stu-id="afa2a-112">Serial Number</span></span>

<span data-ttu-id="afa2a-113">Contiene un numero intero univoco positivo assegnato al certificato dall'Autorità di certificazione (CA).</span><span class="sxs-lookup"><span data-stu-id="afa2a-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="afa2a-114">Algoritmo di firma</span><span class="sxs-lookup"><span data-stu-id="afa2a-114">Signature Algorithm</span></span>

<span data-ttu-id="afa2a-115">Contiene un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) che specifica l'algoritmo usato dall'autorità di certificazione per firmare il certificato.</span><span class="sxs-lookup"><span data-stu-id="afa2a-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="afa2a-116">Ad esempio, 1.2.840.113549.1.1.5 specifica un algoritmo di hash SHA-1 combinato con l'algoritmo di crittografia RSA realizzato da RSA Laboratories.</span><span class="sxs-lookup"><span data-stu-id="afa2a-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a><span data-ttu-id="afa2a-117">Issuer</span><span class="sxs-lookup"><span data-stu-id="afa2a-117">Issuer</span></span>

<span data-ttu-id="afa2a-118">Contiene il nome distinto [*X. 500*](/windows/desktop/SecGloss/x-gly) (DN) dell'autorità di certificazione che ha creato e firmato il certificato.</span><span class="sxs-lookup"><span data-stu-id="afa2a-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a><span data-ttu-id="afa2a-119">Validità</span><span class="sxs-lookup"><span data-stu-id="afa2a-119">Validity</span></span>

<span data-ttu-id="afa2a-120">Specifica l'intervallo di tempo di validità del certificato.</span><span class="sxs-lookup"><span data-stu-id="afa2a-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="afa2a-121">Le date fino alla fine del 2049 usano il formato Coordinated Universal Time (Greenwich Mean Time) (*yymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="afa2a-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="afa2a-122">Le date che iniziano con il 1 ° gennaio 2050 usano il formato di ora generalizzato (*yyyymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="afa2a-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a><span data-ttu-id="afa2a-123">Oggetto</span><span class="sxs-lookup"><span data-stu-id="afa2a-123">Subject</span></span>

<span data-ttu-id="afa2a-124">Contiene un nome distinto X.500 dell'entità associata alla chiave pubblica contenuta nel certificato.</span><span class="sxs-lookup"><span data-stu-id="afa2a-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a><span data-ttu-id="afa2a-125">Chiave pubblica</span><span class="sxs-lookup"><span data-stu-id="afa2a-125">Public Key</span></span>

<span data-ttu-id="afa2a-126">Contiene la chiave pubblica e le informazioni sugli algoritmi associate.</span><span class="sxs-lookup"><span data-stu-id="afa2a-126">Contains the public key and associated algorithm information.</span></span>

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="related-topics"></a><span data-ttu-id="afa2a-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afa2a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa2a-128">Campi versione 2</span><span class="sxs-lookup"><span data-stu-id="afa2a-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="afa2a-129">Estensioni versione 3</span><span class="sxs-lookup"><span data-stu-id="afa2a-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="afa2a-130">Certificati di chiave pubblica X. 509</span><span class="sxs-lookup"><span data-stu-id="afa2a-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
