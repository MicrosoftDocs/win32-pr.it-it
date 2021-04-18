---
description: Le estensioni sono incluse in una \# richiesta di certificato PKCS 10 aggiungendole al campo attributi della struttura CertificationRequestInfo illustrata nell'esempio di sintassi ASN. 1 seguente. Per ulteriori informazioni, vedere l'argomento attributi.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Estensioni PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319370"
---
# <a name="pkcs-10-extensions"></a><span data-ttu-id="1904e-104">\#Estensioni PKCS 10</span><span class="sxs-lookup"><span data-stu-id="1904e-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="1904e-105">Le estensioni sono incluse in una \# richiesta di certificato PKCS 10 aggiungendole al campo **attributi** della struttura **CertificationRequestInfo** illustrata nell'esempio di sintassi ASN. 1 seguente.</span><span class="sxs-lookup"><span data-stu-id="1904e-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="1904e-106">Per ulteriori informazioni, vedere l'argomento [attributi](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="1904e-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="1904e-107">La procedura seguente illustra come usare l'API di registrazione del certificato per aggiungere estensioni a una richiesta di \# certificato PKCS 10:</span><span class="sxs-lookup"><span data-stu-id="1904e-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="1904e-108">Recuperare una raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chiamando la proprietà [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) sull'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="1904e-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="1904e-109">Creare un'estensione usando una delle interfacce disponibili che derivano dall'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="1904e-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="1904e-110">Aggiungere le estensioni create nel passaggio 2 alla raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperata nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="1904e-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1904e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1904e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1904e-112">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1904e-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="1904e-113">Architettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="1904e-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="1904e-114">\#Attributi PKCS 10</span><span class="sxs-lookup"><span data-stu-id="1904e-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="1904e-115">Estensioni</span><span class="sxs-lookup"><span data-stu-id="1904e-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



