---
description: I valori interi vengono codificati in una tripletta TLV che inizia con un valore Tag di 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEGER (API di registrazione certificati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85151947653a66c98b7a030ade7b9ff7b4f5ee87fd84edc4cc52679be296a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904344"
---
# <a name="integer-certificate-enrollment-api"></a>INTEGER (API di registrazione certificati)

I valori interi vengono codificati in una tripletta TLV che inizia con un **valore Tag** di 0x02. Il **campo Value** della tripletta TLV contiene l'intero codificato se è positivo o il complemento dei due se è negativo. Se il numero intero è positivo ma il bit di ordine elevato è impostato su 1, al contenuto viene aggiunto un 0x00 iniziale per indicare che il numero non è negativo. Ad esempio, il byte di ordine 0x8F (10001111) è 1. Viene quindi aggiunto un byte zero iniziale al contenuto, come illustrato nella figura seguente.

![Codifica der del tipo di dati booleano](images/der-tlv-integer.png)

Se il numero intero contiene meno di 128 byte, il campo *Lunghezza* richiede un solo byte per specificare la lunghezza del contenuto. Se il numero intero è maggiore di 127 byte, il bit 7 del campo *Lunghezza* è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per altre informazioni, vedere [Lunghezza codificata e Byte dei valori](about-encoded-length-and-value-bytes.md).

L'esempio seguente, da [PKCS \# 10 Encoded ASN.1,](pkcs--10-encoded-asn-1.md)mostra la codifica per una chiave pubblica a 128 byte. Il primo byte contiene il **valore Tag** per il tipo di **dati INTEGER,** 0x02. Il secondo e il terzo byte contengono il **valore Length.** Il bit 7 del secondo byte è impostato su 1 perché sono presenti più di 127 byte di contenuto. I bit da 0 a 6 del secondo byte specificano il numero di byte finali necessari, in questo caso uno, per specificare in modo accurato la lunghezza del contenuto. Il terzo byte specifica il numero di byte di contenuto, 0x81. Il quarto byte, 0x00, viene aggiunto al contenuto per indicare che l'intero è effettivamente un valore positivo anche se il bit di segno del byte di contenuto iniziale (0x8F) è impostato su 1.

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

Nell'esempio seguente viene illustrato come viene codificato il valore 0x03 integer. Il **byte** tag contiene 0x02 e **length** byte specifica che è presente un byte di contenuto.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



