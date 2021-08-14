---
description: L'API Di registrazione certificati supporta i tipi ASN.1 di base seguenti.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905046"
---
# <a name="basic-types"></a>Tipi di base

L'API Di registrazione certificati supporta i tipi ASN.1 di base seguenti.

## <a name="bit-string"></a>STRINGA DI BIT

Tag di codifica: 0x03

Certreq.exe nome: BIT \_ STRING

Una stringa bit o binaria è una matrice arbitrariamente lunga di bit. I bit specifici possono essere identificati da numeri interi tra parentesi e nomi assegnati come nell'esempio seguente.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Le chiavi e le firme del certificato sono spesso rappresentate come stringhe di bit.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a>BOOLEAN

Tag di codifica: 0x01

Certreq.exe nome: BOOLEAN

Un tipo booleano può contenere uno dei due valori **TRUE** o **FALSE.** L'esempio seguente illustra la struttura ASN.1 per un'estensione del certificato Basic Constraints. Il **campo cA** specifica se un soggetto del certificato è un'autorità di certificazione (CA). La criticità predefinita è **FALSE.**

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a>INTEGER

Tag di codifica: 0x02

Certreq.exe nome: INTEGER

Un intero può in genere essere qualsiasi valore integrale positivo o negativo. L'esempio seguente illustra la struttura ASN.1 per una chiave pubblica RSA. Si noti che **il campo publicExponent** è limitato a un numero intero positivo minore di 4.294.967.296.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a>NULL

Tag di codifica: 0x05

Certreq.exe nome: **NULL**

Un **tipo NULL** contiene un singolo byte 0x00. Può essere usato in qualsiasi punto in cui la richiesta di certificato deve indicare un valore vuoto. Ad esempio, **algorithmIdentifier** è una sequenza che contiene un identificatore di oggetto (OID) e parametri facoltativi.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

Se non sono presenti parametri quando la struttura è codificata, viene usato **NULL** per indicare un valore vuoto.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICATORE DI OGGETTO

Tag di codifica: 0x06

Certreq.exe nome: ID \_ OGGETTO

L'API di registrazione certificati usa gli identificatori di oggetto (OID) come tipo di puntatore universale agli identificatori di algoritmo, agli attributi e ad altri elementi PKI. Gli OID vengono in genere presentati in una stringa decimale tratteggiata, ad esempio "2.16.840.1.101.3.4.1.42". I singoli elementi della stringa, separati da punti, rappresentano archi e lascia in un albero dell'autorità di registrazione che identifica in modo univoco l'oggetto e l'organizzazione che lo ha registrato. Ad esempio, l'OID precedente può essere espanso in joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining mode (CBC).

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a>STRINGA OTTETTO

Tag di codifica: 0x04

Certreq.exe nome: OCTET \_ STRING

Una stringa di ottetti è una matrice di byte arbitrariamente grande. A differenza **del tipo BIT STRING,** tuttavia, non è possibile assegnare nomi a bit e byte specifici nella stringa. La parola ottetto deve essere un modo indipendente dalla piattaforma per fare riferimento a una parola di memoria. Nel contesto dell'API di registrazione certificati, ottetto e byte sono intercambiabili.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



