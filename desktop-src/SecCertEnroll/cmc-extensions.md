---
description: Le estensioni sono incluse in una richiesta CMC aggiungendole alla struttura TaggedAttributes illustrata nell'esempio di sintassi ASN. 1 seguente. Per ulteriori informazioni, vedere l'argomento attributi.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Estensioni CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232661"
---
# <a name="cmc-extensions"></a><span data-ttu-id="2b440-104">Estensioni CMC</span><span class="sxs-lookup"><span data-stu-id="2b440-104">CMC Extensions</span></span>

<span data-ttu-id="2b440-105">Le estensioni sono incluse in una richiesta CMC aggiungendole alla struttura **TaggedAttributes** illustrata nell'esempio di sintassi ASN. 1 seguente.</span><span class="sxs-lookup"><span data-stu-id="2b440-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="2b440-106">Per ulteriori informazioni, vedere l'argomento [attributi](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="2b440-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="2b440-107">Ogni struttura nella raccolta **TaggedAttributes** contiene un ID di tipo Integer, un identificatore di oggetto ASN. 1 (OID) e un set di valori.</span><span class="sxs-lookup"><span data-stu-id="2b440-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="2b440-108">Le estensioni vengono incorporate in una richiesta aggiungendo una struttura **CmcAddExtensions** al campo **valori** .</span><span class="sxs-lookup"><span data-stu-id="2b440-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="2b440-109">Nell'esempio seguente viene illustrata la sintassi della struttura ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="2b440-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="2b440-110">L'identificatore di oggetto è **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="2b440-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

<span data-ttu-id="2b440-111">La procedura seguente illustra come usare l'API di registrazione certificati per aggiungere estensioni a una richiesta di certificato CMC.</span><span class="sxs-lookup"><span data-stu-id="2b440-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="2b440-112">**Per usare l'API di registrazione certificati per aggiungere estensioni a una richiesta di certificato CMC**</span><span class="sxs-lookup"><span data-stu-id="2b440-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="2b440-113">Creare un'estensione usando una delle interfacce disponibili che derivano dall'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) o usare direttamente l'oggetto **IX509Extension** per creare estensioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="2b440-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="2b440-114">Chiamare la proprietà [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) sull'oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) per recuperare una raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="2b440-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="2b440-115">Aggiungere le estensioni create nel passaggio 1 alla raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="2b440-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="2b440-116">Chiamare [**registra**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) per eseguire automaticamente le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b440-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="2b440-117">Recuperare un oggetto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) dall'oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="2b440-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="2b440-118">Creare e inizializzare un oggetto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) usando la raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperata nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="2b440-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="2b440-119">Creare una raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e aggiungervi l'oggetto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="2b440-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="2b440-120">Usare la raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="2b440-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="2b440-121">Aggiungere l'oggetto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) alla raccolta [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="2b440-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b440-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b440-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b440-123">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="2b440-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="2b440-124">Architettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="2b440-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="2b440-125">Attributi CMC</span><span class="sxs-lookup"><span data-stu-id="2b440-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b440-126">Estensioni</span><span class="sxs-lookup"><span data-stu-id="2b440-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



