---
description: Gli attributi vengono inclusi in una richiesta di certificato PKCS 10 aggiungendoli alla struttura CertificationRequestInfo illustrata \# nell'esempio di sintassi ASN.1 seguente.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: Attributi PKCS \# 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993291"
---
# <a name="pkcs-10-attributes"></a>Attributi PKCS \# 10

Gli attributi vengono inclusi in una richiesta di certificato PKCS 10 aggiungendoli alla \# **struttura CertificationRequestInfo** illustrata nell'esempio di sintassi ASN.1 seguente. Per altre informazioni su come aggiungere attributi a una richiesta, vedere [l'argomento Architettura degli](attribute-architecture.md) attributi.

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

L'attributo più comunemente aggiunto a una richiesta PKCS 10 è una raccolta di estensioni versione 3 definite da un \# [**oggetto IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Poiché una richiesta PKCS 10 non contiene un campo a cui è possibile aggiungere direttamente le estensioni, è necessario aggiungere tali estensioni \# come attributo. Gli **attributi ClientId**, **CspProvider**, **OSVersion** e **RenewalCertificate** possono essere aggiunti anche a un argomento PKCS # .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



