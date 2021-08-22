---
description: Il tipo di dati ASN.1 UTF8String viene codificato in una tripletta TLV che inizia con un byte tag di 0x0C.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b51a42d8c2b296b6c3c98c224b0052a7d89d95dbfe92483b852f6a0167b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903457"
---
# <a name="utf8string"></a>UTF8String

Il tipo di dati ASN.1 **UTF8String** viene codificato in una tripletta TLV che inizia con un **byte** tag di 0x0C. L'esempio seguente, dall'argomento [CMC Encoded ASN.1,](cmc-encoded-asn-1.md) illustra come l'attributo **ClientId** viene codificato come integer e tre **tipi UTF8String.** L'identificatore di oggetto per l'attributo è 1.3.6.1.4.1.311.21.20. Le informazioni, che possono essere specificate tramite [**l'interfaccia IX509AttributeClientId,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) includono un numero ID client, il nome del computer DNS (Domain Name System), il nome utente di Gestione account di sicurezza (SAM) e il nome dell'applicazione che ha creato la richiesta di certificato.

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

Se la stringa contiene meno di 128 byte, il campo **Lunghezza** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se la stringa è maggiore di 127 byte, il bit 7 del campo **Lunghezza** è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per altre informazioni, vedere [Lunghezza codificata e Byte dei valori](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



