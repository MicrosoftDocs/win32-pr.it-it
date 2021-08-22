---
description: Il concetto di tipo di dati è fondamentale per lo standard ASN.1 (Abstract Syntax Notation One).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema di tipi ASN.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0b5b9780057229d301bbabcdf2484c66bf06b4313587b0e70a68070885a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905076"
---
# <a name="asn1-type-system"></a>Sistema di tipi ASN.1

Il concetto di tipo di dati è fondamentale per lo standard ASN.1 (Abstract Syntax Notation One). Ogni campo di una struttura di richiesta di certificato è associato a un tipo. Si consideri, ad esempio, la sintassi del certificato PKCS \# 10 ASN.1 illustrata nell'esempio seguente.

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

La struttura delle richieste di alto **livello, CertificationRequestInfo**, è un tipo costituito da una sequenza di altri tipi. Quando un tipo è o contiene solo tipi di base, tipi stringa o **ANY,** non può essere ulteriormente suddiviso. Ad esempio, il campo **della** versione è un **tipo CertificationRequestInfoVersion** che è, a sua volta, un tipo **INTEGER,** un tipo ASN.1 di base non composto da altri tipi.

Un sistema di tipi consente di presentare visivamente la sintassi di una richiesta in modo facilmente comprensibile da parte degli sviluppatori e consente di codificare in modo coerente la richiesta per la trasmissione in una rete. Per altre informazioni sulla codifica, vedere [Distinguished Encoding Rules](distinguished-encoding-rules.md). Per altre informazioni sui tipi ASN.1, vedere gli argomenti seguenti.

[Tipi di base](about-basic-types.md)

Vengono illustrati i tipi di dati seguenti:

* **STRINGA DI BIT**
* **Boolean**
* **INTEGER**
* **NULL**
* **IDENTIFICATORE DI OGGETTO**
* **STRINGA OTTETTO**

[Tipi di stringa](about-string-types.md)

Vengono illustrati i tipi di stringa seguenti:

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Tipi costruiti](about-constructed-types.md)

Vengono illustrati i tipi di dati ASN.1 che possono contenere tipi di base, tipi stringa o altri tipi costruiti.




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica delle richieste di certificato](about-certificate-request-encoding.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Introduzione alla sintassi e alla codifica ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



