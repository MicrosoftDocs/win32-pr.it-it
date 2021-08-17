---
description: Un tipo ASN.1 (Abstract Syntax Notation One) costruito è costituito da tipi di base, tipi stringa o altri tipi costruiti. Ad esempio, un'estensione del certificato X.509 è composta da tre tipi ASN.1 di base, come illustrato nell'esempio seguente.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipi costruiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ed62c4a59bfc0944ad5e31673ab0ea9031c0175014c8fc1c6b6f2cc071b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904490"
---
# <a name="constructed-types"></a>Tipi costruiti

Un tipo ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) costruito è costituito da tipi di base, tipi stringa o altri tipi costruiti. Ad esempio, un'estensione del certificato X.509 è composta da tre tipi ASN.1 di base, come illustrato nell'esempio seguente.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Un'estensione è costituita da [*un*](/windows/desktop/SecGloss/o-gly) identificatore di oggetto (OID), un valore booleano che identifica se l'estensione è critica e una matrice di byte che contiene il valore. L'API di registrazione certificati supporta i tipi ASN.1 costruiti seguenti.

## <a name="sequence-and-sequence-of"></a>SEQUENCE E SEQUENCE OF

Tag di codifica: 0x30

Contiene una serie ordinata di campi di uno o più tipi. I campi possono essere contrassegnati **come OPTIONAL** o **DEFAULT.** Inoltre, per evitare ambiguità durante la decodifica, i campi facoltativi successivi devono differire l'uno dall'altro usando un identificatore univoco (un numero intero tra parentesi quadre, ad esempio 1) e da un campo obbligatorio seguente, come illustrato nell'esempio \[ \] seguente.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

La differenza tra **SEQUENCE** e **SEQUENCE OF** è che gli elementi di un **costrutto SEQUENCE OF** devono essere dello stesso tipo. Vedere l'esempio seguente. Entrambi i costrutti hanno lo stesso valore di tag (0x30) quando vengono codificati.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Un altro modo per esaminare la differenza tra **SEQUENCE** e **SEQUENCE OF** consiste nel confrontarle con le controparti nel linguaggio di programmazione C. Ciò significa che **SEQUENCE** equivale approssimativamente a una struttura e **SEQUENCE OF** equivale approssimativamente a una matrice.

## <a name="set-and-set-of"></a>SET e SET OF

Tag di codifica: 0x31

Contiene una serie non ordinata di campi di uno o più tipi. Questo comportamento è diverso da **sequence** che contiene un elenco ordinato. Se si specifica un elenco non ordinato, un'applicazione può fornire i campi della struttura al codificatore nell'ordine più appropriato. Come per **SEQUENCE,** i campi di un costrutto **SET** possono essere contrassegnati con **OPTIONAL** o **DEFAULT** e gli identificatori univoci devono essere usati per disambiguare il processo di decodifica. La differenza tra **SET** e **SET OF** è che gli elementi di un **costrutto SET OF** devono essere dello stesso tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>Scelta

Tag di codifica: non applicabile

Definisce una scelta tra alternative. Ogni alternativa deve essere identificata in modo univoco da un intero tra parentesi per evitare ambiguità durante la decodifica. Quando viene codificato, il **costrutto CHOICE** avrà il valore del tag di codifica dell'alternativa scelta.

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
