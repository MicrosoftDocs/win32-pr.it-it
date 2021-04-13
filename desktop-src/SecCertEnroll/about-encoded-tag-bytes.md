---
description: Il campo tag in una tripletta TLV identifica il tipo di struttura dei dati da inviare tra i computer.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Byte tag codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561032"
---
# <a name="encoded-tag-bytes"></a>Byte tag codificati

Il campo *tag* in una tripletta TLV identifica il tipo di struttura dei dati da inviare tra i computer. Ad esempio, il tag per un valore integer è 0x02 e il tag per un identificatore di oggetto è 0x06. Sebbene siano consentiti più byte, nessuno dei tipi di dati usati dall'API di registrazione certificati ne richiede più di uno. Nella figura seguente viene illustrata la suddivisione di un valore di *tag* . Bits 7 e 6 identificano la classe di tag ASN. 1. Sono disponibili quattro classi, ma l'API di registrazione certificati usa tipi di dati che appartengono solo alla classe universale. Bit 5 indica se il formato di codifica è primitivo o costruito. I tipi di base e di stringa sono codificati tramite forme primitive, tipi costruiti usando un formato costruito. Per ulteriori informazioni, vedere [sistema di tipi ASN. 1](about-asn-1-type-system.md). I bit da 4 a 0 contengono il numero di tag.

![byte di tag di der TLV](images/der-tlv-tagbyte.png)

La tabella seguente elenca i tipi di dati supportati dall'API di registrazione del certificato, il modulo di codifica usato e il valore del tag.

| Tipo              | Classe ASN. 1 | Formato di codifica | Valore del tag                             |
|-------------------|-------------|---------------|---------------------------------------|
| STRINGA DI BIT        | UNIVERSAL   | Primitiva     | 00000011<br/> 0x03<br/> |
| BOOLEAN           | UNIVERSAL   | Primitiva     | 00000001<br/> 0x01<br/> |
| INTEGER           | UNIVERSAL   | Primitiva     | 00000010<br/> 0x02<br/> |
| NULL              | UNIVERSAL   | Primitiva     | 00000101<br/> 0x05<br/> |
| IDENTIFICATORE OGGETTO | UNIVERSAL   | Primitiva     | 00000110<br/> 0x06<br/> |
| STRINGA OTTETTO      | UNIVERSAL   | Primitiva     | 00000100<br/> 0x04<br/> |
| BMPString         | UNIVERSAL   | Primitiva     | 00011110<br/> 0x1E<br/> |
| IA5String         | UNIVERSAL   | Primitiva     | 00010110<br/> 0x16<br/> |
| PrintableString   | UNIVERSAL   | Primitiva     | 00010011<br/> 0x13<br/> |
| TeletexString     | UNIVERSAL   | Primitiva     | 00010100<br/> 0x14<br/> |
| UTF8String        | UNIVERSAL   | Primitiva     | 00001100<br/> 0X0C<br/> |
| SEQUENCE          | UNIVERSAL   | Costruito   | 00110000<br/> 0x30<br/> |
| SEQUENZA DI       | UNIVERSAL   | Costruito   | 00110000<br/> 0x30<br/> |
| SET               | UNIVERSAL   | Costruito   | 00110001<br/> 0x31<br/> |
| SET DI            | UNIVERSAL   | Costruito   | 00110001<br/> 0x31<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi di trasferimento DER](about-der-transfer-syntax.md)
</dt> <dt>

[Byte di lunghezza e valore codificati](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




