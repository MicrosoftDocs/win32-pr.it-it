---
description: Utilizzato per aggiungere attributi a una richiesta di certificato.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Architettura degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344951"
---
# <a name="attribute-architecture"></a><span data-ttu-id="59c09-103">Architettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="59c09-103">Attribute Architecture</span></span>

<span data-ttu-id="59c09-104">Per aggiungere attributi a una richiesta di certificato, vengono utilizzate le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="59c09-104">The following interfaces are used to add attributes to a certificate request:</span></span>

-   [<span data-ttu-id="59c09-105">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="59c09-105">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="59c09-106">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="59c09-106">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="59c09-107">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="59c09-107">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="59c09-108">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="59c09-108">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

<span data-ttu-id="59c09-109">L'architettura segue quello definito nel modulo ASN. 1 della \# sintassi della richiesta di certificazione PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="59c09-109">The architecture follows that defined in the ASN.1 module of the PKCS \#10 certification request syntax.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="59c09-110">La raccolta [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) corrisponde al campo **Attributes** e ogni oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) nella raccolta corrisponde a una struttura dell' **attributo** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="59c09-110">The [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection corresponds to the **attributes** field, and each [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object in the collection corresponds to an ASN.1 **Attribute** structure.</span></span>

<span data-ttu-id="59c09-111">Ogni **attributo** è costituito da un identificatore di oggetto (OID) e da zero o più valori associati all'OID.</span><span class="sxs-lookup"><span data-stu-id="59c09-111">Each **Attribute** consists of an object identifier (OID) and zero or more values associated with the OID.</span></span> <span data-ttu-id="59c09-112">Una singola coppia OID-valore è rappresentata da un'interfaccia [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="59c09-112">A single OID-value pair is represented by an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) interface.</span></span> <span data-ttu-id="59c09-113">È possibile usare una raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) , ma ogni attributo della raccolta deve essere associato allo stesso OID.</span><span class="sxs-lookup"><span data-stu-id="59c09-113">You can use an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object, but each attribute in the collection must be associated with the same OID.</span></span> <span data-ttu-id="59c09-114">In genere, un attributo ha un solo valore.</span><span class="sxs-lookup"><span data-stu-id="59c09-114">Typically, an attribute has only one value.</span></span>

<span data-ttu-id="59c09-115">È possibile usare una delle interfacce seguenti, che derivano da [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), per creare una singola coppia di attributi OID/valore:</span><span class="sxs-lookup"><span data-stu-id="59c09-115">You can use any of the following interfaces, which derive from [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), to create a single OID/value attribute pair:</span></span>

-   [<span data-ttu-id="59c09-116">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="59c09-116">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="59c09-117">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="59c09-117">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="59c09-118">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="59c09-118">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="59c09-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="59c09-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="59c09-120">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="59c09-120">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="59c09-121">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="59c09-121">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="59c09-122">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="59c09-122">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="59c09-123">Ad esempio, la procedura seguente illustra come creare un attributo **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="59c09-123">For example, the following procedure shows how to create a **ClientId** attribute.</span></span>

<span data-ttu-id="59c09-124">\*\*Per creare un attributo \*\*ClientID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="59c09-124">**To create a **ClientId** attribute**</span></span>

1.  <span data-ttu-id="59c09-125">Recuperare un oggetto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) da un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="59c09-125">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
2.  <span data-ttu-id="59c09-126">Creare e inizializzare un oggetto [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="59c09-126">Create and initialize an [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
3.  <span data-ttu-id="59c09-127">Creare una raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e aggiungere l'oggetto [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="59c09-127">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
4.  <span data-ttu-id="59c09-128">Usare la raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="59c09-128">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
5.  <span data-ttu-id="59c09-129">Aggiungere l'oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) alla raccolta recuperata nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="59c09-129">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the collection retrieved in step 1.</span></span>

<span data-ttu-id="59c09-130">Nell'esempio seguente viene illustrato l'output ASN. 1 dell'attributo **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="59c09-130">The following example shows the ASN.1 output of the **ClientId** attribute.</span></span> <span data-ttu-id="59c09-131">L'attributo contiene il nome DNS del computer in cui è stata generata la richiesta (test3d.jdomcsc.nttest.microsoft.com), il nome SAM dell'utente (amministratore JDOMCSC \\ ) e il nome dell'applicazione che ha generato la richiesta (certreq).</span><span class="sxs-lookup"><span data-stu-id="59c09-131">The attribute contains the DNS name of the computer on which the request was generated (test3d.jdomcsc.nttest.microsoft.com), the SAM name of the user (JDOMCSC\\administrator), and the name of the application that generated the request (certreq).</span></span>

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a><span data-ttu-id="59c09-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59c09-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59c09-133">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="59c09-133">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="59c09-134">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="59c09-134">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="59c09-135">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="59c09-135">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="59c09-136">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="59c09-136">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



