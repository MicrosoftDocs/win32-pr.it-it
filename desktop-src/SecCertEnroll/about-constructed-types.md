---
description: Un tipo costruito Abstract Syntax Notation One (ASN. 1) è costituito da tipi di base, tipi stringa o altri tipi costruiti. Ad esempio, un'estensione del certificato X. 509 è composta da tre tipi ASN. 1 di base, come illustrato nell'esempio seguente.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipi costruiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306472"
---
# <a name="constructed-types"></a>Tipi costruiti

Un tipo costruito [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) è costituito da tipi di base, tipi stringa o altri tipi costruiti. Ad esempio, un'estensione del certificato X. 509 è composta da tre tipi ASN. 1 di base, come illustrato nell'esempio seguente.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Un'estensione è costituita da un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID), un valore booleano che indica se l'estensione è critica e una matrice di byte che contiene il valore. L'API di registrazione certificati supporta i tipi ASN. 1 costruiti seguenti.

## <a name="sequence-and-sequence-of"></a>SEQUENZA e sequenza di

Tag di codifica: 0x30

Contiene una serie ordinata di campi di uno o più tipi. I campi possono essere contrassegnati come **facoltativi** o **predefiniti**. Inoltre, per evitare ambiguità durante la decodifica, i campi facoltativi successivi devono essere diversi l'uno dall'altro usando un identificatore univoco (un intero racchiuso tra parentesi, ad esempio \[ 1 \] ) e da un campo obbligatorio seguente, come illustrato nell'esempio seguente.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

La differenza tra **sequenza** e **sequenza di** è che gli elementi di una **sequenza di** costrutto devono essere dello stesso tipo. Vedere l'esempio seguente. Entrambi i costrutti hanno lo stesso valore di tag (0x30) quando vengono codificati.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Un altro modo per esaminare la differenza tra **sequenza** e **sequenza di** consiste nel confrontarli con le rispettive controparti nel linguaggio di programmazione C. Ovvero la **sequenza** è approssimativamente equivalente a una struttura e la **sequenza di** è approssimativamente equivalente a una matrice.

## <a name="set-and-set-of"></a>SET e SET di

Tag di codifica: 0x31

Contiene una serie non ordinata di campi di uno o più tipi. Questo comportamento è diverso da una **sequenza** che contiene un elenco ordinato. La specifica di un elenco non ordinato consente a un'applicazione di fornire i campi della struttura al codificatore nell'ordine più appropriato. Come per la **sequenza**, i campi di un costrutto **set** possono essere contrassegnati con **facoltativo** o **default** e gli identificatori univoci devono essere usati per evitare ambiguità nel processo di decodifica. La differenza tra **set** e **set di** è che gli elementi di un **set di** costrutto devono essere dello stesso tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>SCELTA

Tag di codifica: non applicabile

Definisce una scelta tra alternative. Ogni alternativa deve essere identificata in modo univoco da un intero racchiuso tra parentesi quadre per evitare ambiguità durante la decodifica. Una volta codificato, il costrutto **Choice** avrà il valore del tag di codifica dell'alternativa scelta.

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

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
