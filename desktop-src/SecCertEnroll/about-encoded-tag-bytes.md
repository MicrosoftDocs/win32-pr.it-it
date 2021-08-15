---
description: Il campo Tag in una tripletta TLV identifica il tipo di struttura dei dati inviata tra computer.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Byte tag codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27face1fe04cf52c79d6c4047f87f58e98f2bc1a7b7656109341c9ce2be59d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904324"
---
# <a name="encoded-tag-bytes"></a>Byte tag codificati

Il *campo Tag* in una tripletta TLV identifica il tipo di struttura dei dati inviata tra computer. Ad esempio, il tag per un numero intero 0x02 e il tag per un identificatore di oggetto è 0x06. Sebbene siano consentiti più byte, nessuno dei tipi di dati usati dall'API di registrazione certificati ne richiede più di uno. La figura seguente mostra la suddivisione di un *valore Tag.* I bit 7 e 6 identificano la classe di tag ASN.1. Sono disponibili quattro classi, ma l'API di registrazione certificati usa tipi di dati che appartengono solo alla classe UNIVERSAL. Il bit 5 identifica se il formato di codifica è primitivo o costruito. I tipi di base e stringa vengono codificati usando forme primitive, tipi costruiti usando un formato costruito. Per altre informazioni, vedere [Sistema dei tipi ASN.1.](about-asn-1-type-system.md) I bit da 4 a 0 contengono il numero di tag.

![der tlv tag byte](images/der-tlv-tagbyte.png)

La tabella seguente elenca i tipi di dati supportati dall'API di registrazione certificati, il modulo di codifica usato e il valore del tag.

| Tipo              | Classe ASN.1 | Modulo di codifica | Valore del tag                             |
|-------------------|-------------|---------------|---------------------------------------|
| STRINGA DI BIT        | Universale   | Primitiva     | 00000011<br/> (0x03)<br/> |
| BOOLEAN           | Universale   | Primitiva     | 00000001<br/> (0x01)<br/> |
| INTEGER           | Universale   | Primitiva     | 00000010<br/> (0x02)<br/> |
| NULL              | Universale   | Primitiva     | 00000101<br/> (0x05)<br/> |
| IDENTIFICATORE DI OGGETTO | Universale   | Primitiva     | 00000110<br/> (0x06)<br/> |
| OCTET STRING      | Universale   | Primitiva     | 00000100<br/> (0x04)<br/> |
| BMPString         | Universale   | Primitiva     | 00011110<br/> (0x1E)<br/> |
| IA5String         | Universale   | Primitiva     | 00010110<br/> (0x16)<br/> |
| PrintableString   | Universale   | Primitiva     | 00010011<br/> (0x13)<br/> |
| TeletexString     | Universale   | Primitiva     | 00010100<br/> (0x14)<br/> |
| UTF8String        | Universale   | Primitiva     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | Universale   | Costruito   | 00110000<br/> (0x30)<br/> |
| SEQUENZA DI       | Universale   | Costruito   | 00110000<br/> (0x30)<br/> |
| SET               | Universale   | Costruito   | 00110001<br/> (0x31)<br/> |
| SET OF            | Universale   | Costruito   | 00110001<br/> (0x31)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi di trasferimento DER](about-der-transfer-syntax.md)
</dt> <dt>

[Lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




