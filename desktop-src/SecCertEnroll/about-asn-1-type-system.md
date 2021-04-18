---
description: Il concetto di tipo di dati è fondamentale per lo standard Abstract Syntax Notation One (ASN. 1).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema di tipi ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319385"
---
# <a name="asn1-type-system"></a><span data-ttu-id="2bd0a-103">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2bd0a-103">ASN.1 Type System</span></span>

<span data-ttu-id="2bd0a-104">Il concetto di tipo di dati è fondamentale per lo standard Abstract Syntax Notation One (ASN. 1).</span><span class="sxs-lookup"><span data-stu-id="2bd0a-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="2bd0a-105">Ogni campo di una struttura di richiesta di certificato è associato a un tipo.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="2bd0a-106">Si consideri, ad esempio, la \# sintassi del certificato PKCS 10 ASN. 1 illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
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

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="2bd0a-107">La struttura di richiesta di alto livello, **CertificationRequestInfo**, è un tipo costituito da una sequenza di altri tipi.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="2bd0a-108">Quando un tipo è o contiene solo tipi di base, tipi stringa o **qualsiasi**, non può essere suddiviso ulteriormente.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="2bd0a-109">Ad esempio, il campo **Version** è un tipo **CertificationRequestInfoVersion** , che a sua volta è un tipo **Integer** , un tipo ASN. 1 di base che non è composto da altri tipi.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="2bd0a-110">Un sistema di tipi consente di presentare visivamente la sintassi di una richiesta in modo prontamente comprensibile agli sviluppatori e consente la codifica coerente della richiesta per la trasmissione in una rete.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="2bd0a-111">Per ulteriori informazioni sulla codifica, vedere [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span><span class="sxs-lookup"><span data-stu-id="2bd0a-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="2bd0a-112">Per ulteriori informazioni sui tipi ASN. 1, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="2bd0a-113">Tipi di base</span><span class="sxs-lookup"><span data-stu-id="2bd0a-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="2bd0a-114">Vengono descritti i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-114">Discusses the following data types:</span></span>

* <span data-ttu-id="2bd0a-115">**STRINGA DI BIT**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-115">**BIT STRING**</span></span>
* <span data-ttu-id="2bd0a-116">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-116">**BOOLEAN**</span></span>
* <span data-ttu-id="2bd0a-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-117">**INTEGER**</span></span>
* <span data-ttu-id="2bd0a-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-118">**NULL**</span></span>
* <span data-ttu-id="2bd0a-119">**IDENTIFICATORE OGGETTO**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="2bd0a-120">**STRINGA OTTETTO**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-120">**OCTET STRING**</span></span>

[<span data-ttu-id="2bd0a-121">Tipi di stringa</span><span class="sxs-lookup"><span data-stu-id="2bd0a-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="2bd0a-122">Vengono illustrati i tipi di stringa seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-122">Discusses the following string types:</span></span>

* <span data-ttu-id="2bd0a-123">**BMPString**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-123">**BMPString**</span></span>
* <span data-ttu-id="2bd0a-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-124">**IA5String**</span></span>
* <span data-ttu-id="2bd0a-125">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-125">**PrintableString**</span></span>
* <span data-ttu-id="2bd0a-126">**TeletexString**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-126">**TeletexString**</span></span>
* <span data-ttu-id="2bd0a-127">**UTF8String**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-127">**UTF8String**</span></span>

[<span data-ttu-id="2bd0a-128">Tipi costruiti</span><span class="sxs-lookup"><span data-stu-id="2bd0a-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="2bd0a-129">Vengono descritti i tipi di dati ASN. 1 che possono contenere tipi di base, tipi stringa o altri tipi costruiti.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="2bd0a-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bd0a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd0a-131">Codifica della richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="2bd0a-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="2bd0a-132">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2bd0a-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="2bd0a-133">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="2bd0a-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="2bd0a-134">Introduzione alla sintassi e alla codifica ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2bd0a-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



