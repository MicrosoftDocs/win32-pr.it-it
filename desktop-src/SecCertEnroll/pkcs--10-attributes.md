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
# <a name="pkcs-10-attributes"></a>\#Attributi PKCS 10

Gli attributi sono inclusi in una \# richiesta di certificato PKCS 10 aggiungendoli alla struttura **CertificationRequestInfo** illustrata nell'esempio di sintassi ASN. 1 riportato di seguito. Per ulteriori informazioni su come è possibile aggiungere attributi a una richiesta, vedere l'argomento relativo all' [architettura dell'attributo](attribute-architecture.md) .

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

L'attributo aggiunto più di frequente a una \# richiesta PKCS 10 è costituito da una raccolta di estensioni della versione 3 definite da un oggetto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Poiché una \# richiesta PKCS 10 non contiene un campo a cui è possibile aggiungere direttamente le estensioni, è necessario aggiungerle come attributo. Gli attributi **ClientID**, **CspProvider**, **OSVersion** e **RenewalCertificate** possono essere aggiunti anche a un argomento Pkcs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



