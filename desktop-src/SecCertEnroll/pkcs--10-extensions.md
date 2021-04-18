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
# <a name="pkcs-10-extensions"></a>\#Estensioni PKCS 10

Le estensioni sono incluse in una \# richiesta di certificato PKCS 10 aggiungendole al campo **attributi** della struttura **CertificationRequestInfo** illustrata nell'esempio di sintassi ASN. 1 seguente. Per ulteriori informazioni, vedere l'argomento [attributi](attributes.md) .

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

La procedura seguente illustra come usare l'API di registrazione del certificato per aggiungere estensioni a una richiesta di \# certificato PKCS 10:

1.  Recuperare una raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chiamando la proprietà [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) sull'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
2.  Creare un'estensione usando una delle interfacce disponibili che derivano dall'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .
3.  Aggiungere le estensioni create nel passaggio 2 alla raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperata nel passaggio 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributes (Attributi)](attributes.md)
</dt> <dt>

[Architettura degli attributi](attribute-architecture.md)
</dt> <dt>

[\#Attributi PKCS 10](pkcs--10-attributes.md)
</dt> <dt>

[Estensioni](extensions.md)
</dt> </dl>

 

 



