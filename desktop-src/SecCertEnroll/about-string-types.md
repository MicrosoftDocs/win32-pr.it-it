---
description: Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) è la creazione di un nome distinto X.500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9e190e10bc86bd68a344f5aa279b4812bc04437418578320c36e0e1791dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903690"
---
# <a name="string-types"></a>Tipi di stringa

Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) è la creazione di un nome distinto X.500. Ad esempio, il nome soggetto di una richiesta di certificato viene creato combinando una sequenza di nomi distinti relativi, come illustrato nell'esempio di sintassi seguente.

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

L'API Di registrazione certificati supporta i tipi di stringa ASN.1 seguenti.

## <a name="bmpstring"></a>BMPString

Tag di codifica: 0x1E

Certreq.exe nome: \_ STRINGA UNICODE

Basic Multilingual Plane (BMP) è una codifica dei caratteri che comprende il primo piano del set di caratteri universali (UCS). Sono presenti diciassette piani numerati da 0 a 16. BMP occupa il piano 0 e include 65.536 punti di codice da 0x0000 a 0xFFFF. Questa è la sezione della mappa caratteri Unicode in cui finora è stata effettuata la maggior parte delle assegnazioni di caratteri. Include latino, medio oriente, asia, africa e altre lingue.

## <a name="ia5string"></a>IA5String

Tag di codifica: 0x16

Certreq.exe nome: IA5 \_ STRING

L'alfabeto internazionale numero 5 (IA5) è in genere equivalente all'alfabeto ASCII, ma versioni diverse possono includere accenti o altri caratteri specifici di una lingua dell'area. L'esempio seguente illustra il **tipo IA5String** usato nella definizione ASN.1 dell'estensione del certificato **AlternativeNames.**

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a>PrintableString

Tag di codifica: 0x13

Certreq.exe nome: PRINTABLE \_ STRING

Il **tipo di dati PrintableString** era originariamente destinato a rappresentare i set di caratteri limitati disponibili per i terminali di input mainframe, ma viene comunque usato comunemente. Contiene i caratteri seguenti:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Tag di codifica: 0x14

I tipi di dati **TeletexString** e **T61String** correlati vengono codificati a 8 bit (o a 16 bit per i caratteri compositi). Entrambi hanno un numero di tag di 0x14. Non vengono usate in modo approfondito.

## <a name="utf8string"></a>UTF8String

Tag di codifica: 0x0C

Certreq.exe nome: UTF8 \_ STRING

Il formato di trasformazione UCS/Unicode a 8 bit (UTF-8) è una codifica di caratteri a lunghezza variabile che può rappresentare qualsiasi carattere universale come carattere Unicode, consentendo al tempo stesso ai punti di codice iniziali di rimanere coerenti con ASCII. UTF-8 usa da uno a quattro byte. Il numero di tag è 0x0C.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



