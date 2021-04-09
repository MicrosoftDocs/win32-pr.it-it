---
description: Il tipo di dati UTF8String ASN. 1 è codificato in una tripletta TLV che inizia con un byte di tag di 0x0C.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26048a46689d27b68e8cacfa4af13b37cde4d613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881665"
---
# <a name="utf8string"></a>UTF8String

Il tipo di dati **UTF8STRING** ASN. 1 è codificato in una tripletta TLV che inizia con un byte di **tag** di 0x0C. Nell'esempio seguente, dall'argomento [ASN. 1 con codifica CMC](cmc-encoded-asn-1.md) , viene illustrato come l'attributo **ClientID** è codificato come numero intero e tre tipi di **utf8string** . L'identificatore di oggetto per l'attributo è 1.3.6.1.4.1.311.21.20. Le informazioni che è possibile specificare tramite l'interfaccia [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) includono un numero ID client, il nome del computer Domain Name System (DNS), il nome utente di gestione degli account di sicurezza (Sam) e il nome dell'applicazione che ha creato la richiesta di certificato.

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

Se la stringa contiene meno di 128 byte, il campo **lunghezza** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se la stringa è maggiore di 127 byte, il bit 7 del campo **lunghezza** è impostato su 1 e BITS 6-0 specifica il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per ulteriori informazioni, vedere [lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



