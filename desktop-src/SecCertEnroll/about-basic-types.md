---
description: L'API di registrazione certificati supporta i tipi ASN. 1 di base seguenti.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311936"
---
# <a name="basic-types"></a>Tipi di base

L'API di registrazione certificati supporta i tipi ASN. 1 di base seguenti.

## <a name="bit-string"></a>STRINGA DI BIT

Tag di codifica: 0x03

Nome Certreq.exe: stringa di BIT \_

Una stringa bit o binaria è una matrice di bit arbitrariamente lungo. I bit specifici possono essere identificati da numeri interi racchiusi tra parentesi e nomi assegnati come nell'esempio seguente.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Le firme e le chiavi del certificato sono spesso rappresentate come stringhe di bit.

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

Nome Certreq.exe: BOOLEAN

Un tipo Boolean può contenere uno dei due valori **true** o **false**. Nell'esempio seguente viene illustrata la struttura ASN. 1 per un'estensione del certificato di vincoli di base. Il campo **CA** specifica se un soggetto del certificato è un'autorità di certificazione (CA). La criticità predefinita è **false**.

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

Nome Certreq.exe: INTEGER

Un Integer può in genere essere un valore integrale positivo o negativo. Nell'esempio seguente viene illustrata la struttura ASN. 1 per una chiave pubblica RSA. Si noti che il campo **publicExponent** è limitato a un numero intero positivo inferiore a 4.294.967.296.

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

Nome Certreq.exe: **null**

Un tipo **null** contiene un solo byte 0x00. Può essere usato in qualsiasi punto in cui la richiesta di certificato deve indicare un valore vuoto. Ad esempio, un **AlgorithmIdentifier** è una sequenza che contiene un identificatore di oggetto (OID) e parametri facoltativi.

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

Se non sono presenti parametri quando la struttura è codificata, viene usato **null** per indicare un valore vuoto.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICATORE OGGETTO

Tag di codifica: 0x06

Nome Certreq.exe: \_ ID oggetto

L'API di registrazione del certificato usa gli identificatori di oggetto (OID) come tipo di puntatore universale per gli identificatori di algoritmo, gli attributi e altri elementi dell'infrastruttura a chiave pubblica. OID vengono in genere presentati in una stringa decimale tratteggiata, ad esempio "2.16.840.1.101.3.4.1.42". I singoli elementi nella stringa, separati da punti, rappresentano gli archi e lascia in un albero dell'autorità di registrazione che identifica in modo univoco l'oggetto e l'organizzazione che lo ha registrato. L'OID precedente, ad esempio, può essere espanso a joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) con. 42 accodato per identificare in modo univoco l'algoritmo della modalità CBC (AES Cipher Block Chain) a 256 bit.

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

Nome Certreq.exe: \_ stringa ottetto

Una stringa di ottetto è una matrice di byte arbitrariamente grande. A differenza del tipo di **stringa bit** , tuttavia, i bit e i byte specifici nella stringa non possono essere assegnati a nomi. Il termine ottetto è concepito come un modo indipendente dalla piattaforma per fare riferimento a una parola di memoria. All'interno del contesto dell'API di registrazione del certificato, l'ottetto e il byte sono intercambiabili.

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

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



