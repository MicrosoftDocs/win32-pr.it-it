---
description: Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) consiste nel creare un nome distinto X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231504"
---
# <a name="string-types"></a>Tipi di stringa

Uno degli usi più comuni delle stringhe in un'infrastruttura a chiave pubblica (PKI) consiste nel creare un nome distinto X. 500. Il nome soggetto di una richiesta di certificato, ad esempio, viene creato combinando una sequenza di nomi distinti relativi, come illustrato nell'esempio di sintassi seguente.

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

L'API di registrazione certificati supporta i tipi di stringa ASN. 1 seguenti.

## <a name="bmpstring"></a>BMPString

Tag di codifica: 0x1E

Nome Certreq.exe: \_ stringa Unicode

Il piano multilingue di base (BMP) è una codifica dei caratteri che comprende il primo piano del set di caratteri universali (UCS). Sono disponibili diciassette piani numerati da 0 a 16. BMP occupa il piano 0 e include 65.536 punti di codice da 0x0000 a 0xFFFF. Questa è la sezione della mappa dei caratteri Unicode in cui la maggior parte delle assegnazioni di caratteri è stata finora eseguita. Sono inclusi il latino, Medio Oriente, asiatico, africano e altri linguaggi.

## <a name="ia5string"></a>IA5String

Tag di codifica: 0x16

Nome Certreq.exe: \_ stringa IA5

L'alfabeto internazionale numero 5 (IA5) è in genere equivalente all'alfabeto ASCII, ma versioni diverse possono includere accenti o altri caratteri specifici di una lingua regionale. Nell'esempio seguente viene illustrato il tipo **IA5String** utilizzato nella definizione ASN. 1 dell'estensione del certificato **AlternativeNames** .

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

Nome Certreq.exe: stringa STAMPAbile \_

Il tipo di dati **PrintableString** è stato originariamente progettato per rappresentare i set di caratteri limitati disponibili per i terminali di input del mainframe, ma viene comunque utilizzato comunemente. Contiene i caratteri seguenti:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Tag di codifica: 0x14

I tipi di dati **TeletexString** e **T61String** correlati vengono codificati su 8 bit (o 16 bit per i caratteri compositi). Entrambi hanno un numero di Tag pari a 0x14. Non vengono usati ampiamente.

## <a name="utf8string"></a>UTF8String

Tag di codifica: 0x0C

Nome Certreq.exe: \_ stringa UTF8

Il formato di trasformazione UCS/Unicode a 8 bit (UTF-8) è una codifica dei caratteri a lunghezza variabile che può rappresentare qualsiasi carattere universale come carattere Unicode, consentendo in tal modo che i punti di codice iniziali rimangano coerenti con ASCII. UTF-8 USA da uno a quattro byte. Il numero di tag è 0x0C.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



