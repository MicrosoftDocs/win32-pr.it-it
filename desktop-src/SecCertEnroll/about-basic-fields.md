---
description: Un certificato X. 509 versione 1 contiene i campi seguenti. I campi della versione 2 sono illustrati nei campi della versione 2. I campi della versione 3 sono illustrati nelle estensioni della versione 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881681"
---
# <a name="basic-fields"></a>Campi di base

Un certificato X. 509 versione 1 contiene i campi seguenti. I campi della versione 2 sono illustrati nei [campi della versione 2](about-version-2-fields.md). I campi della versione 3 sono illustrati nelle [estensioni della versione 3](about-version-3-extensions.md).

## <a name="version"></a>Versione

Specifica il numero di versione del certificato codificato. Attualmente, i valori possibili di questo campo sono 0, 1 o 2, ma questo può essere espanso in futuro.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Numero di serie

Contiene un numero intero univoco positivo assegnato al certificato dall'Autorità di certificazione (CA).

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Algoritmo di firma

Contiene un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) che specifica l'algoritmo usato dall'autorità di certificazione per firmare il certificato. Ad esempio, 1.2.840.113549.1.1.5 specifica un algoritmo di hash SHA-1 combinato con l'algoritmo di crittografia RSA realizzato da RSA Laboratories.

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a>Issuer

Contiene il nome distinto [*X. 500*](/windows/desktop/SecGloss/x-gly) (DN) dell'autorità di certificazione che ha creato e firmato il certificato.

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a>Validità

Specifica l'intervallo di tempo di validità del certificato. Le date fino alla fine del 2049 usano il formato Coordinated Universal Time (Greenwich Mean Time) (*yymmddhhmmssZ*). Le date che iniziano con il 1 ° gennaio 2050 usano il formato di ora generalizzato (*yyyymmddhhmmssZ*).

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a>Oggetto

Contiene un nome distinto X.500 dell'entità associata alla chiave pubblica contenuta nel certificato.

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a>Chiave pubblica

Contiene la chiave pubblica e le informazioni sugli algoritmi associate.

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Campi versione 2](about-version-2-fields.md)
</dt> <dt>

[Estensioni versione 3](about-version-3-extensions.md)
</dt> <dt>

[Certificati di chiave pubblica X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
