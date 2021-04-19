---
description: L'API di registrazione certificati supporta i tipi ASN. 1 di base seguenti.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311936"
---
# <a name="basic-types"></a><span data-ttu-id="ac242-103">Tipi di base</span><span class="sxs-lookup"><span data-stu-id="ac242-103">Basic Types</span></span>

<span data-ttu-id="ac242-104">L'API di registrazione certificati supporta i tipi ASN. 1 di base seguenti.</span><span class="sxs-lookup"><span data-stu-id="ac242-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="ac242-105">STRINGA DI BIT</span><span class="sxs-lookup"><span data-stu-id="ac242-105">BIT STRING</span></span>

<span data-ttu-id="ac242-106">Tag di codifica: 0x03</span><span class="sxs-lookup"><span data-stu-id="ac242-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="ac242-107">Nome Certreq.exe: stringa di BIT \_</span><span class="sxs-lookup"><span data-stu-id="ac242-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="ac242-108">Una stringa bit o binaria è una matrice di bit arbitrariamente lungo.</span><span class="sxs-lookup"><span data-stu-id="ac242-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="ac242-109">I bit specifici possono essere identificati da numeri interi racchiusi tra parentesi e nomi assegnati come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="ac242-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="ac242-110">Le firme e le chiavi del certificato sono spesso rappresentate come stringhe di bit.</span><span class="sxs-lookup"><span data-stu-id="ac242-110">Certificate keys and signatures are often represented as bit strings.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a><span data-ttu-id="ac242-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac242-111">BOOLEAN</span></span>

<span data-ttu-id="ac242-112">Tag di codifica: 0x01</span><span class="sxs-lookup"><span data-stu-id="ac242-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="ac242-113">Nome Certreq.exe: BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac242-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="ac242-114">Un tipo Boolean può contenere uno dei due valori **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="ac242-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="ac242-115">Nell'esempio seguente viene illustrata la struttura ASN. 1 per un'estensione del certificato di vincoli di base.</span><span class="sxs-lookup"><span data-stu-id="ac242-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="ac242-116">Il campo **CA** specifica se un soggetto del certificato è un'autorità di certificazione (CA).</span><span class="sxs-lookup"><span data-stu-id="ac242-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="ac242-117">La criticità predefinita è **false**.</span><span class="sxs-lookup"><span data-stu-id="ac242-117">The default criticality is **FALSE**.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a><span data-ttu-id="ac242-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="ac242-118">INTEGER</span></span>

<span data-ttu-id="ac242-119">Tag di codifica: 0x02</span><span class="sxs-lookup"><span data-stu-id="ac242-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="ac242-120">Nome Certreq.exe: INTEGER</span><span class="sxs-lookup"><span data-stu-id="ac242-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="ac242-121">Un Integer può in genere essere un valore integrale positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ac242-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="ac242-122">Nell'esempio seguente viene illustrata la struttura ASN. 1 per una chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="ac242-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="ac242-123">Si noti che il campo **publicExponent** è limitato a un numero intero positivo inferiore a 4.294.967.296.</span><span class="sxs-lookup"><span data-stu-id="ac242-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a><span data-ttu-id="ac242-124">NULL</span><span class="sxs-lookup"><span data-stu-id="ac242-124">NULL</span></span>

<span data-ttu-id="ac242-125">Tag di codifica: 0x05</span><span class="sxs-lookup"><span data-stu-id="ac242-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="ac242-126">Nome Certreq.exe: **null**</span><span class="sxs-lookup"><span data-stu-id="ac242-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="ac242-127">Un tipo **null** contiene un solo byte 0x00.</span><span class="sxs-lookup"><span data-stu-id="ac242-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="ac242-128">Può essere usato in qualsiasi punto in cui la richiesta di certificato deve indicare un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="ac242-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="ac242-129">Ad esempio, un **AlgorithmIdentifier** è una sequenza che contiene un identificatore di oggetto (OID) e parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ac242-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

<span data-ttu-id="ac242-130">Se non sono presenti parametri quando la struttura è codificata, viene usato **null** per indicare un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="ac242-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="ac242-131">IDENTIFICATORE OGGETTO</span><span class="sxs-lookup"><span data-stu-id="ac242-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="ac242-132">Tag di codifica: 0x06</span><span class="sxs-lookup"><span data-stu-id="ac242-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="ac242-133">Nome Certreq.exe: \_ ID oggetto</span><span class="sxs-lookup"><span data-stu-id="ac242-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="ac242-134">L'API di registrazione del certificato usa gli identificatori di oggetto (OID) come tipo di puntatore universale per gli identificatori di algoritmo, gli attributi e altri elementi dell'infrastruttura a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="ac242-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="ac242-135">OID vengono in genere presentati in una stringa decimale tratteggiata, ad esempio "2.16.840.1.101.3.4.1.42".</span><span class="sxs-lookup"><span data-stu-id="ac242-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="ac242-136">I singoli elementi nella stringa, separati da punti, rappresentano gli archi e lascia in un albero dell'autorità di registrazione che identifica in modo univoco l'oggetto e l'organizzazione che lo ha registrato.</span><span class="sxs-lookup"><span data-stu-id="ac242-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="ac242-137">L'OID precedente, ad esempio, può essere espanso a joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) con. 42 accodato per identificare in modo univoco l'algoritmo della modalità CBC (AES Cipher Block Chain) a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="ac242-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a><span data-ttu-id="ac242-138">STRINGA OTTETTO</span><span class="sxs-lookup"><span data-stu-id="ac242-138">OCTET STRING</span></span>

<span data-ttu-id="ac242-139">Tag di codifica: 0x04</span><span class="sxs-lookup"><span data-stu-id="ac242-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="ac242-140">Nome Certreq.exe: \_ stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="ac242-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="ac242-141">Una stringa di ottetto è una matrice di byte arbitrariamente grande.</span><span class="sxs-lookup"><span data-stu-id="ac242-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="ac242-142">A differenza del tipo di **stringa bit** , tuttavia, i bit e i byte specifici nella stringa non possono essere assegnati a nomi.</span><span class="sxs-lookup"><span data-stu-id="ac242-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="ac242-143">Il termine ottetto è concepito come un modo indipendente dalla piattaforma per fare riferimento a una parola di memoria.</span><span class="sxs-lookup"><span data-stu-id="ac242-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="ac242-144">All'interno del contesto dell'API di registrazione del certificato, l'ottetto e il byte sono intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="ac242-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a><span data-ttu-id="ac242-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac242-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac242-146">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ac242-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="ac242-147">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="ac242-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="ac242-148">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ac242-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



