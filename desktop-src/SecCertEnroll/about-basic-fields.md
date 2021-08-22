---
description: Un certificato X.509 versione 1 contiene i campi seguenti. I campi della versione 2 sono descritti in Campi versione 2. I campi della versione 3 sono descritti nelle estensioni della versione 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3dae9ceaa3ddd1c4ac8a8ce86425ec32eee45e82ca8b437ed0f0c27f44817ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905086"
---
# <a name="basic-fields"></a>Campi di base

Un certificato X.509 versione 1 contiene i campi seguenti. I campi della versione 2 sono descritti in [Campi versione 2.](about-version-2-fields.md) I campi della versione 3 sono descritti in [Estensioni della versione 3.](about-version-3-extensions.md)

## <a name="version"></a>Versione

Specifica il numero di versione del certificato codificato. Attualmente, i valori possibili di questo campo sono 0, 1 o 2, ma potrebbero essere espansi in futuro.

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

Contiene un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) che specifica l'algoritmo usato dalla CA per firmare il certificato. Ad esempio, 1.2.840.113549.1.1.5 specifica un algoritmo di hash SHA-1 combinato con l'algoritmo di crittografia RSA realizzato da RSA Laboratories.

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

Contiene il [*nome distinto X.500*](/windows/desktop/SecGloss/x-gly) della CA che ha creato e firmato il certificato.

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

Specifica l'intervallo di tempo di validità del certificato. Le date fino alla fine del 2049 usano il formato Coordinated Universal Time (ora media di Greenwich) (*yymmddhhmmssz*). Le date che iniziano con il 1° gennaio 2050 usano il formato ora generalizzato (*aaaammgghhmmssz*).

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

[Certificati a chiave pubblica X.509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
