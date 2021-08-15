---
description: Il tipo di dati ASN.1 OCTET STRING viene codificato in una tripletta TLV che inizia con un byte Tag di 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: OCTET STRING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588547e5211efbe6b4b91a8a72f6644de0c7c4dcbacc570f0a1f272e7cc97962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903745"
---
# <a name="octet-string"></a>OCTET STRING

Il tipo di dati ASN.1 **OCTET STRING** viene codificato in una tripletta TLV che inizia con un byte **Tag** di 0x04. I **tipi di dati OCTET STRING** e BIT [STRING](about-bit-string.md) sono molto simili. Di conseguenza, i due tipi vengono codificati in modo simile, ad eccezione del fatto che, poiché il byte finale di **una STRINGA OCTET** non può avere bit inutilizzati, non è necessario aggiungere byte iniziali al contenuto. L'esempio seguente, adattato dall'argomento [CMC Encoded ASN.1](cmc-encoded-asn-1.md) ,mostra come il nome di un modello di certificato viene codificato come matrice di byte.

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

Se la matrice di byte contiene meno di 128 byte, il campo **Length** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se è maggiore di 127 byte, il bit 7 del campo **Length** è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Questo è illustrato nell'esempio seguente in cui il bit di ordine superiore del secondo byte nella prima riga è impostato su 1 e il byte indica che è presente un byte **length** finale. Il terzo byte specifica quindi che il contenuto è lungo 0x80 byte.

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



