---
description: Il tipo di dati IA5tring ASN. 1 è codificato in una tripletta TLV che inizia con un byte di tag di 0x16.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7562fab655462455b03d35041bdb8f572b064cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231512"
---
# <a name="ia5string"></a>IA5String

Il tipo di dati **IA5TRING** ASN. 1 è codificato in una tripletta TLV che inizia con un byte di **tag** di 0x16. Nell'esempio seguente, adattato dall'argomento [ASN. 1 con codifica CMC](cmc-encoded-asn-1.md) , viene illustrato il modo in cui l'attributo **OSVersion** è codificato come tipo **IA5tring** . Il numero di versione può essere specificato tramite l'interfaccia [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) . L'identificatore di oggetto per l'attributo è 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Se la stringa contiene meno di 128 byte, il campo **lunghezza** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se la stringa è maggiore di 127 byte, il bit 7 del campo **lunghezza** è impostato su 1 e BITS 6-0 specifica il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per ulteriori informazioni, vedere [lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



