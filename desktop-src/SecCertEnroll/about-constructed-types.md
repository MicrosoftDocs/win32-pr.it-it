---
description: Un tipo costruito Abstract Syntax Notation One (ASN. 1) è costituito da tipi di base, tipi stringa o altri tipi costruiti. Ad esempio, un'estensione del certificato X. 509 è composta da tre tipi ASN. 1 di base, come illustrato nell'esempio seguente.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipi costruiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306472"
---
# <a name="constructed-types"></a><span data-ttu-id="4d303-104">Tipi costruiti</span><span class="sxs-lookup"><span data-stu-id="4d303-104">Constructed Types</span></span>

<span data-ttu-id="4d303-105">Un tipo costruito [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) è costituito da tipi di base, tipi stringa o altri tipi costruiti.</span><span class="sxs-lookup"><span data-stu-id="4d303-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="4d303-106">Ad esempio, un'estensione del certificato X. 509 è composta da tre tipi ASN. 1 di base, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="4d303-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="4d303-107">Un'estensione è costituita da un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID), un valore booleano che indica se l'estensione è critica e una matrice di byte che contiene il valore.</span><span class="sxs-lookup"><span data-stu-id="4d303-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="4d303-108">L'API di registrazione certificati supporta i tipi ASN. 1 costruiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d303-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="4d303-109">SEQUENZA e sequenza di</span><span class="sxs-lookup"><span data-stu-id="4d303-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="4d303-110">Tag di codifica: 0x30</span><span class="sxs-lookup"><span data-stu-id="4d303-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="4d303-111">Contiene una serie ordinata di campi di uno o più tipi.</span><span class="sxs-lookup"><span data-stu-id="4d303-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="4d303-112">I campi possono essere contrassegnati come **facoltativi** o **predefiniti**.</span><span class="sxs-lookup"><span data-stu-id="4d303-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="4d303-113">Inoltre, per evitare ambiguità durante la decodifica, i campi facoltativi successivi devono essere diversi l'uno dall'altro usando un identificatore univoco (un intero racchiuso tra parentesi, ad esempio \[ 1 \] ) e da un campo obbligatorio seguente, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="4d303-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="4d303-114">La differenza tra **sequenza** e **sequenza di** è che gli elementi di una **sequenza di** costrutto devono essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="4d303-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="4d303-115">Vedere l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="4d303-115">See the following example.</span></span> <span data-ttu-id="4d303-116">Entrambi i costrutti hanno lo stesso valore di tag (0x30) quando vengono codificati.</span><span class="sxs-lookup"><span data-stu-id="4d303-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="4d303-117">Un altro modo per esaminare la differenza tra **sequenza** e **sequenza di** consiste nel confrontarli con le rispettive controparti nel linguaggio di programmazione C.</span><span class="sxs-lookup"><span data-stu-id="4d303-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="4d303-118">Ovvero la **sequenza** è approssimativamente equivalente a una struttura e la **sequenza di** è approssimativamente equivalente a una matrice.</span><span class="sxs-lookup"><span data-stu-id="4d303-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="4d303-119">SET e SET di</span><span class="sxs-lookup"><span data-stu-id="4d303-119">SET and SET OF</span></span>

<span data-ttu-id="4d303-120">Tag di codifica: 0x31</span><span class="sxs-lookup"><span data-stu-id="4d303-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="4d303-121">Contiene una serie non ordinata di campi di uno o più tipi.</span><span class="sxs-lookup"><span data-stu-id="4d303-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="4d303-122">Questo comportamento è diverso da una **sequenza** che contiene un elenco ordinato.</span><span class="sxs-lookup"><span data-stu-id="4d303-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="4d303-123">La specifica di un elenco non ordinato consente a un'applicazione di fornire i campi della struttura al codificatore nell'ordine più appropriato.</span><span class="sxs-lookup"><span data-stu-id="4d303-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="4d303-124">Come per la **sequenza**, i campi di un costrutto **set** possono essere contrassegnati con **facoltativo** o **default** e gli identificatori univoci devono essere usati per evitare ambiguità nel processo di decodifica.</span><span class="sxs-lookup"><span data-stu-id="4d303-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="4d303-125">La differenza tra **set** e **set di** è che gli elementi di un **set di** costrutto devono essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="4d303-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="4d303-126">SCELTA</span><span class="sxs-lookup"><span data-stu-id="4d303-126">CHOICE</span></span>

<span data-ttu-id="4d303-127">Tag di codifica: non applicabile</span><span class="sxs-lookup"><span data-stu-id="4d303-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="4d303-128">Definisce una scelta tra alternative.</span><span class="sxs-lookup"><span data-stu-id="4d303-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="4d303-129">Ogni alternativa deve essere identificata in modo univoco da un intero racchiuso tra parentesi quadre per evitare ambiguità durante la decodifica.</span><span class="sxs-lookup"><span data-stu-id="4d303-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="4d303-130">Una volta codificato, il costrutto **Choice** avrà il valore del tag di codifica dell'alternativa scelta.</span><span class="sxs-lookup"><span data-stu-id="4d303-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a><span data-ttu-id="4d303-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d303-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d303-132">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4d303-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="4d303-133">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4d303-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="4d303-134">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="4d303-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
