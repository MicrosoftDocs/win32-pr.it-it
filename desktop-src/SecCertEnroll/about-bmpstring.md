---
description: Il tipo di dati ASN.1 BMPString, denominato STRINGA UNICODE nell'API di registrazione certificati, viene codificato in una tripletta TLV che inizia con un byte tag di \_ 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 496715d380739dd68dab4266422876ecca174b9caffd3895e9c465f446d32cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904840"
---
# <a name="bmpstring"></a>BMPString

Il tipo di dati ASN.1 **BMPString,** denominato **\_ STRINGA UNICODE** nell'API di registrazione certificati, viene codificato in una tripletta TLV che inizia con un byte **tag** di 0x1E. L'esempio seguente, adattato dall'argomento [CMC Encoded ASN.1](cmc-encoded-asn-1.md) , mostra la codifica per un'estensione **TemplateName.** Il nome può essere specificato usando [**l'interfaccia IX509ExtensionTemplateName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) L'identificatore di oggetto per l'estensione è 1.3.6.1.4.1.311.13.2.1.

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

Se la stringa contiene meno di 128 byte, il campo **Length** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto. Se la stringa è maggiore di 127 byte, il bit 7 del campo **Length** è impostato su 1 e i bit da 6 a 0 specificano il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto. Per altre informazioni, vedere [Lunghezza codificata e Byte valore.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



