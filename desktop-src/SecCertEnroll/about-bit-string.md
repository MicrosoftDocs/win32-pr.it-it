---
description: Il tipo di dati BIT STRING viene codificato in una tripletta TLV che inizia con un byte Tag 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: STRINGA DI BIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056616a22cf2e683e943afef9369ed4c885963174aff0e72dea6ef718ddbdf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905062"
---
# <a name="bit-string"></a>STRINGA DI BIT

Il **tipo di dati BIT STRING** viene codificato in una tripletta TLV che inizia con un byte **Tag** 0x03. Il **campo Value** della tripletta TLV contiene un byte iniziale che specifica il numero di bit rimasti inutilizzati nel byte finale del contenuto. Nell'esempio seguente il campo **Length** è impostato su 0x03 perché seguono tre byte di contenuto e il byte iniziale del campo **Value** è impostato su 0x04 perché sono presenti quattro bit inutilizzati nell'ultimo byte di contenuto. Ogni bit inutilizzato è denotato dalla lettera x.

![Codifica der del tipo di dati stringa di bit](images/der-tlv-bitstring.png)

L'esempio seguente, adattato dall'argomento [ \# PKCS 10 Encoded ASN.1 (ASN con codifica PKCS 10),](pkcs--10-encoded-asn-1.md) mostra la firma codificata di una richiesta di certificato PKCS \# 10 di esempio. Il primo byte contiene il **valore Tag** per il tipo di dati **BIT STRING,** 0x03. Il secondo e il terzo byte contengono la lunghezza della matrice di byte. Il bit 7 del secondo byte è impostato su 1 perché sono presenti più di 127 byte di contenuto. I bit da 0 a 6 del secondo byte specificano il numero di byte **di lunghezza** finali, in questo caso uno. Il terzo byte specifica il numero di byte di contenuto, 0x81. Il quarto byte, 0x00, specifica il numero di bit inutilizzati presenti nell'ultimo byte di contenuto. Si noti che la firma è codificata nell'ordine dei byte big endian.

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



