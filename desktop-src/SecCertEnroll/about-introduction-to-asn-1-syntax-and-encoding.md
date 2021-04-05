---
description: L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per definire, codificare e decodificare le richieste di certificati e i certificati trasferiti tra i computer client e le autorità di certificazione.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introduzione alla sintassi e alla codifica ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881674"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="e93d0-103">Introduzione alla sintassi e alla codifica ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e93d0-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="e93d0-104">L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per definire, codificare e decodificare le richieste di certificati e i certificati trasferiti tra i computer client e le autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="e93d0-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="e93d0-105">ASN. 1 può essere concettualmente suddiviso in un set di regole di sintassi e un set di regole di codifica, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e93d0-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="e93d0-106">Esempio di sintassi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e93d0-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="e93d0-107">Una richiesta di certificato contiene, tra le altre cose, il nome dell'entità che sta effettuando la richiesta o per la quale viene effettuata la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e93d0-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="e93d0-108">Il nome è una sequenza di X. 500 nomi distinti relativi (RDNs).</span><span class="sxs-lookup"><span data-stu-id="e93d0-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="e93d0-109">Ogni RDN nella sequenza è costituito da un identificatore di oggetto (OID) e da un valore.</span><span class="sxs-lookup"><span data-stu-id="e93d0-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="e93d0-110">Nell'esempio seguente viene illustrata la sintassi ASN. 1 per un nome soggetto.</span><span class="sxs-lookup"><span data-stu-id="e93d0-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="e93d0-111">Esempio di codifica ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e93d0-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="e93d0-112">L'API di registrazione certificati USA [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) per codificare il nome soggetto precedente.</span><span class="sxs-lookup"><span data-stu-id="e93d0-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="e93d0-113">DER richiede che ogni elemento nel nome sia rappresentato da una tripletta TLV, dove T contiene il numero di tag del tipo ASN. 1, L contiene la lunghezza e V contiene il valore associato.</span><span class="sxs-lookup"><span data-stu-id="e93d0-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="e93d0-114">Nell'esempio seguente viene illustrato il modo in cui il nome soggetto TestCN. TestOrg è codificato.</span><span class="sxs-lookup"><span data-stu-id="e93d0-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="e93d0-115">Tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e93d0-115">Note the following points:</span></span>

-   <span data-ttu-id="e93d0-116">Riga 1:</span><span class="sxs-lookup"><span data-stu-id="e93d0-116">Line 1:</span></span><dl> <span data-ttu-id="e93d0-117">Il nome è una sequenza di nomi distinti relativi.</span><span class="sxs-lookup"><span data-stu-id="e93d0-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="e93d0-118">Il numero di tag per il tipo di **sequenza** è 0x30.</span><span class="sxs-lookup"><span data-stu-id="e93d0-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="e93d0-119">Il nome soggetto di TestCN. TestOrg richiede 35 byte (0x23).</span><span class="sxs-lookup"><span data-stu-id="e93d0-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="e93d0-120">Il nome comune, TestCN, è un singolo set di strutture **AttributeTypeValue** .</span><span class="sxs-lookup"><span data-stu-id="e93d0-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="e93d0-121">Il numero di tag per un **set** è 0x31.</span><span class="sxs-lookup"><span data-stu-id="e93d0-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="e93d0-122">
-   Riga 3:</span><span class="sxs-lookup"><span data-stu-id="e93d0-122">
-   Line 3:</span></span><dl> <span data-ttu-id="e93d0-123">La struttura **AttributeTypeValue** è una sequenza.</span><span class="sxs-lookup"><span data-stu-id="e93d0-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="e93d0-124">Il numero di tag per il tipo di **sequenza** è 0x30.</span><span class="sxs-lookup"><span data-stu-id="e93d0-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="e93d0-125">La struttura richiede 13 (0xD) byte.</span><span class="sxs-lookup"><span data-stu-id="e93d0-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="e93d0-126">
-   Righe da 4 a 6:</span><span class="sxs-lookup"><span data-stu-id="e93d0-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="e93d0-127">L'identificatore di oggetto (OID) per il nome comune è 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="e93d0-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="e93d0-128">L'OID è un tipo di **\_ ID oggetto** a tre byte.</span><span class="sxs-lookup"><span data-stu-id="e93d0-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="e93d0-129">Il numero di tag per il tipo di **\_ ID oggetto** è 0x06.</span><span class="sxs-lookup"><span data-stu-id="e93d0-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="e93d0-130">
-   Righe da 7 a 9:</span><span class="sxs-lookup"><span data-stu-id="e93d0-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="e93d0-131">Il nome comune, TestCN, è un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="e93d0-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="e93d0-132">La stringa è un tipo di **\_ stringa stampabile** a sei byte.</span><span class="sxs-lookup"><span data-stu-id="e93d0-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="e93d0-133">Il numero di tag per il tipo di **\_ stringa stampabile** è 0x13.</span><span class="sxs-lookup"><span data-stu-id="e93d0-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="e93d0-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e93d0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e93d0-135">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e93d0-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="e93d0-136">Codifica della richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="e93d0-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="e93d0-137">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e93d0-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="e93d0-138">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="e93d0-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
