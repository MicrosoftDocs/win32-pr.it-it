---
description: Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) consiste nel creare un nome distinto X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231504"
---
# <a name="string-types"></a><span data-ttu-id="8a10a-103">Tipi di stringa</span><span class="sxs-lookup"><span data-stu-id="8a10a-103">String Types</span></span>

<span data-ttu-id="8a10a-104">Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) consiste nel creare un nome distinto X. 500.</span><span class="sxs-lookup"><span data-stu-id="8a10a-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="8a10a-105">Il nome soggetto di una richiesta di certificato, ad esempio, viene creato combinando una sequenza di nomi distinti relativi, come illustrato nell'esempio di sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="8a10a-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="8a10a-106">L'API di registrazione certificati supporta i tipi di stringa ASN. 1 seguenti.</span><span class="sxs-lookup"><span data-stu-id="8a10a-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="8a10a-107">BMPString</span><span class="sxs-lookup"><span data-stu-id="8a10a-107">BMPString</span></span>

<span data-ttu-id="8a10a-108">Tag di codifica: 0x1E</span><span class="sxs-lookup"><span data-stu-id="8a10a-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="8a10a-109">Nome Certreq.exe: \_ stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="8a10a-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="8a10a-110">Il piano multilingue di base (BMP) è una codifica dei caratteri che comprende il primo piano del set di caratteri universali (UCS).</span><span class="sxs-lookup"><span data-stu-id="8a10a-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="8a10a-111">Sono disponibili diciassette piani numerati da 0 a 16.</span><span class="sxs-lookup"><span data-stu-id="8a10a-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="8a10a-112">BMP occupa il piano 0 e include 65.536 punti di codice da 0x0000 a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="8a10a-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="8a10a-113">Questa è la sezione della mappa dei caratteri Unicode in cui la maggior parte delle assegnazioni di caratteri è stata finora eseguita.</span><span class="sxs-lookup"><span data-stu-id="8a10a-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="8a10a-114">Sono inclusi il latino, Medio Oriente, asiatico, africano e altri linguaggi.</span><span class="sxs-lookup"><span data-stu-id="8a10a-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="8a10a-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="8a10a-115">IA5String</span></span>

<span data-ttu-id="8a10a-116">Tag di codifica: 0x16</span><span class="sxs-lookup"><span data-stu-id="8a10a-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="8a10a-117">Nome Certreq.exe: \_ stringa IA5</span><span class="sxs-lookup"><span data-stu-id="8a10a-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="8a10a-118">L'alfabeto internazionale numero 5 (IA5) è in genere equivalente all'alfabeto ASCII, ma versioni diverse possono includere accenti o altri caratteri specifici di una lingua regionale.</span><span class="sxs-lookup"><span data-stu-id="8a10a-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="8a10a-119">Nell'esempio seguente viene illustrato il tipo **IA5String** utilizzato nella definizione ASN. 1 dell'estensione del certificato **AlternativeNames** .</span><span class="sxs-lookup"><span data-stu-id="8a10a-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a><span data-ttu-id="8a10a-120">PrintableString</span><span class="sxs-lookup"><span data-stu-id="8a10a-120">PrintableString</span></span>

<span data-ttu-id="8a10a-121">Tag di codifica: 0x13</span><span class="sxs-lookup"><span data-stu-id="8a10a-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="8a10a-122">Nome Certreq.exe: stringa STAMPAbile \_</span><span class="sxs-lookup"><span data-stu-id="8a10a-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="8a10a-123">Il tipo di dati **PrintableString** è stato originariamente progettato per rappresentare i set di caratteri limitati disponibili per i terminali di input del mainframe, ma viene comunque utilizzato comunemente.</span><span class="sxs-lookup"><span data-stu-id="8a10a-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="8a10a-124">Contiene i caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a10a-124">It contains the following characters:</span></span>

-   <span data-ttu-id="8a10a-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="8a10a-125">A-Z</span></span>
-   <span data-ttu-id="8a10a-126">a-z</span><span class="sxs-lookup"><span data-stu-id="8a10a-126">a-z</span></span>
-   <span data-ttu-id="8a10a-127">0-9</span><span class="sxs-lookup"><span data-stu-id="8a10a-127">0-9</span></span>
-   <span data-ttu-id="8a10a-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="8a10a-128">' ( ) + , - .</span></span> <span data-ttu-id="8a10a-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="8a10a-129">/ : = ?</span></span> <span data-ttu-id="8a10a-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="8a10a-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="8a10a-131">TeletexString</span><span class="sxs-lookup"><span data-stu-id="8a10a-131">TeletexString</span></span>

<span data-ttu-id="8a10a-132">Tag di codifica: 0x14</span><span class="sxs-lookup"><span data-stu-id="8a10a-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="8a10a-133">I tipi di dati **TeletexString** e **T61String** correlati vengono codificati su 8 bit (o 16 bit per i caratteri compositi).</span><span class="sxs-lookup"><span data-stu-id="8a10a-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="8a10a-134">Entrambi hanno un numero di Tag pari a 0x14.</span><span class="sxs-lookup"><span data-stu-id="8a10a-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="8a10a-135">Non vengono usati ampiamente.</span><span class="sxs-lookup"><span data-stu-id="8a10a-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="8a10a-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="8a10a-136">UTF8String</span></span>

<span data-ttu-id="8a10a-137">Tag di codifica: 0x0C</span><span class="sxs-lookup"><span data-stu-id="8a10a-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="8a10a-138">Nome Certreq.exe: \_ stringa UTF8</span><span class="sxs-lookup"><span data-stu-id="8a10a-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="8a10a-139">Il formato di trasformazione UCS/Unicode a 8 bit (UTF-8) è una codifica dei caratteri a lunghezza variabile che può rappresentare qualsiasi carattere universale come carattere Unicode, consentendo in tal modo che i punti di codice iniziali rimangano coerenti con ASCII.</span><span class="sxs-lookup"><span data-stu-id="8a10a-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="8a10a-140">UTF-8 USA da uno a quattro byte.</span><span class="sxs-lookup"><span data-stu-id="8a10a-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="8a10a-141">Il numero di tag è 0x0C.</span><span class="sxs-lookup"><span data-stu-id="8a10a-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a10a-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a10a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a10a-143">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8a10a-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="8a10a-144">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="8a10a-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="8a10a-145">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8a10a-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



