---
description: Sequence contiene un campo ordinato di uno o più tipi.
ms.assetid: b1a37cde-d5a2-4b01-a076-cb09741ae51d
title: SEQUENCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1362fd66180d6f85926e1c0fe0ae57cc0edbf5edc770283ef7d9eae81cbd7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903700"
---
# <a name="sequence"></a>SEQUENCE

Sequence **contiene** un campo ordinato di uno o più tipi. Viene codificato in una tripletta TLV che inizia con un byte **tag** di 0x30. L'output Certutil.exe seguente dell'argomento [ \# PKCS 10 Encoded ASN.1 (ASN con codifica PKCS 10)](pkcs--10-encoded-asn-1.md) fornisce diversi esempi di strutture di dati **SEQUENCE.** L'output mostra una chiave pubblica a 128 byte e un esponente a tre byte.

``` syntax
30 81 9f                             ; SEQUENCE (9f Bytes)
|  30 0d                             ; SEQUENCE (d Bytes)
|  |  |  06 09                       ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01 01  ; 1.2.840.113549.1.1.1 
|  |  05 00                          ; NULL (0 Bytes)
|  03 81 8d                          ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                       ; SEQUENCE (89 Bytes)
|        02 81 81                    ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                       ; INTEGER (3 Bytes)
|           01 00 01
```

Se **SEQUENCE contiene** meno di 128 byte, il campo **Length** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se è maggiore di 127 byte, il bit 7 del campo **Length** è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Ad esempio, il secondo byte della prima riga nell'esempio precedente indica che è presente un byte **length** finale  che specifica 0x9F byte di contenuto (la maggior parte della sequenza non viene visualizzata). Per altre informazioni, vedere [Lunghezza codificata e Byte valore.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



