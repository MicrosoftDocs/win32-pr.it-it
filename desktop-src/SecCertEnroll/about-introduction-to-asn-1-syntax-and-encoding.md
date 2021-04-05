---
description: L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per definire, codificare e decodificare le richieste di certificati e i certificati trasferiti tra i computer client e le autorità di certificazione.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introduzione alla sintassi e alla codifica ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881674"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Introduzione alla sintassi e alla codifica ASN. 1

L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per definire, codificare e decodificare le richieste di certificati e i certificati trasferiti tra i computer client e le autorità di certificazione. ASN. 1 può essere concettualmente suddiviso in un set di regole di sintassi e un set di regole di codifica, come illustrato negli esempi seguenti.

## <a name="asn1-syntax-example"></a>Esempio di sintassi ASN. 1

Una richiesta di certificato contiene, tra le altre cose, il nome dell'entità che sta effettuando la richiesta o per la quale viene effettuata la richiesta. Il nome è una sequenza di X. 500 nomi distinti relativi (RDNs). Ogni RDN nella sequenza è costituito da un identificatore di oggetto (OID) e da un valore. Nell'esempio seguente viene illustrata la sintassi ASN. 1 per un nome soggetto.

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a>Esempio di codifica ASN. 1

L'API di registrazione certificati USA [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) per codificare il nome soggetto precedente. DER richiede che ogni elemento nel nome sia rappresentato da una tripletta TLV, dove T contiene il numero di tag del tipo ASN. 1, L contiene la lunghezza e V contiene il valore associato. Nell'esempio seguente viene illustrato il modo in cui il nome soggetto TestCN. TestOrg è codificato.

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

Tenere presente quanto segue:

-   Riga 1:<dl> Il nome è una sequenza di nomi distinti relativi.  
    Il numero di tag per il tipo di **sequenza** è 0x30.  
    Il nome soggetto di TestCN. TestOrg richiede 35 byte (0x23).  
    </dl>
-   Line 2:<dl> Il nome comune, TestCN, è un singolo set di strutture **AttributeTypeValue** .  
    Il numero di tag per un **set** è 0x31.  
    </dl>
-   Riga 3:<dl> La struttura **AttributeTypeValue** è una sequenza.  
    Il numero di tag per il tipo di **sequenza** è 0x30.  
    La struttura richiede 13 (0xD) byte.  
    </dl>
-   Righe da 4 a 6:<dl> L'identificatore di oggetto (OID) per il nome comune è 2.5.4.3.  
    L'OID è un tipo di **\_ ID oggetto** a tre byte.  
    Il numero di tag per il tipo di **\_ ID oggetto** è 0x06.  
    </dl>
-   Righe da 7 a 9:<dl> Il nome comune, TestCN, è un valore stringa.  
    La stringa è un tipo di **\_ stringa stampabile** a sei byte.  
    Il numero di tag per il tipo di **\_ stringa stampabile** è 0x13.  
    </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica della richiesta di certificato](about-certificate-request-encoding.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
