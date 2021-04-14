---
description: Gli attributi sono inclusi in una \# richiesta di certificato PKCS 10 aggiungendoli alla struttura CertificationRequestInfo illustrata nell'esempio di sintassi ASN. 1 riportato di seguito.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Attributi PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350186"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="c342c-103">\#Attributi PKCS 10</span><span class="sxs-lookup"><span data-stu-id="c342c-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="c342c-104">Gli attributi sono inclusi in una \# richiesta di certificato PKCS 10 aggiungendoli alla struttura **CertificationRequestInfo** illustrata nell'esempio di sintassi ASN. 1 riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c342c-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="c342c-105">Per ulteriori informazioni su come è possibile aggiungere attributi a una richiesta, vedere l'argomento relativo all' [architettura dell'attributo](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="c342c-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

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

<span data-ttu-id="c342c-106">L'attributo aggiunto più di frequente a una \# richiesta PKCS 10 è costituito da una raccolta di estensioni della versione 3 definite da un oggetto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="c342c-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="c342c-107">Poiché una \# richiesta PKCS 10 non contiene un campo a cui è possibile aggiungere direttamente le estensioni, è necessario aggiungerle come attributo.</span><span class="sxs-lookup"><span data-stu-id="c342c-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="c342c-108">Gli attributi **ClientID**, **CspProvider**, **OSVersion** e **RenewalCertificate** possono essere aggiunti anche a un argomento Pkcs.</span><span class="sxs-lookup"><span data-stu-id="c342c-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c342c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c342c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c342c-110">Attributi supportati</span><span class="sxs-lookup"><span data-stu-id="c342c-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



