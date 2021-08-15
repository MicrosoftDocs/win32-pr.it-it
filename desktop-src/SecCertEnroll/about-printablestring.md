---
description: Il tipo di dati ASN.1 PrintableString viene codificato in una tripletta TLV che inizia con un byte Tag di 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903753"
---
# <a name="printablestring"></a>PrintableString

Il tipo di dati ASN.1 **PrintableString** viene codificato in una tripletta TLV che inizia con un byte **Tag** di 0x13. L'esempio seguente, nell'argomento [ \# PKCS 10 Encoded ASN.1 (ASN con codifica PKCS 10),](pkcs--10-encoded-asn-1.md) illustra come un nome comune utente di TestCN viene codificato come **tipo PrintableString.** L'identificatore di oggetto per un nome comune è 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Se la stringa contiene meno di 128 byte, il campo **Length** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se la stringa è maggiore di 127 byte, il bit 7 del campo **Length** è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per altre informazioni, vedere [Lunghezza codificata e Byte valore.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



