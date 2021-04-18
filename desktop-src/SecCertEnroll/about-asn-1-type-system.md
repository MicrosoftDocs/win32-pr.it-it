---
description: Il concetto di tipo di dati è fondamentale per lo standard Abstract Syntax Notation One (ASN. 1).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema di tipi ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319385"
---
# <a name="asn1-type-system"></a>Sistema di tipi ASN. 1

Il concetto di tipo di dati è fondamentale per lo standard Abstract Syntax Notation One (ASN. 1). Ogni campo di una struttura di richiesta di certificato è associato a un tipo. Si consideri, ad esempio, la \# sintassi del certificato PKCS 10 ASN. 1 illustrato nell'esempio seguente.

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

La struttura di richiesta di alto livello, **CertificationRequestInfo**, è un tipo costituito da una sequenza di altri tipi. Quando un tipo è o contiene solo tipi di base, tipi stringa o **qualsiasi**, non può essere suddiviso ulteriormente. Ad esempio, il campo **Version** è un tipo **CertificationRequestInfoVersion** , che a sua volta è un tipo **Integer** , un tipo ASN. 1 di base che non è composto da altri tipi.

Un sistema di tipi consente di presentare visivamente la sintassi di una richiesta in modo prontamente comprensibile agli sviluppatori e consente la codifica coerente della richiesta per la trasmissione in una rete. Per ulteriori informazioni sulla codifica, vedere [Distinguished Encoding Rules](distinguished-encoding-rules.md). Per ulteriori informazioni sui tipi ASN. 1, vedere gli argomenti seguenti.

[Tipi di base](about-basic-types.md)

Vengono descritti i tipi di dati seguenti:

* **STRINGA DI BIT**
* **BOOLEAN**
* **INTEGER**
* **NULL**
* **IDENTIFICATORE OGGETTO**
* **STRINGA OTTETTO**

[Tipi di stringa](about-string-types.md)

Vengono illustrati i tipi di stringa seguenti:

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Tipi costruiti](about-constructed-types.md)

Vengono descritti i tipi di dati ASN. 1 che possono contenere tipi di base, tipi stringa o altri tipi costruiti.




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica della richiesta di certificato](about-certificate-request-encoding.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Introduzione alla sintassi e alla codifica ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



