---
description: La tabella seguente contiene i valori restituiti che possono essere restituiti dalle funzioni che eseguono la codifica o la decodifica ASN.1 (Abstract Syntax Notation One).
ms.assetid: cb1f34dd-dab4-4ffb-a73b-79a214290509
title: Codifica/decodifica dei valori restituiti ASN.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c48bc5bc122f322650c7913ea9d1978d5113da31fa650a23e8f439555d7ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880101"
---
# <a name="asn1-encodingdecoding-return-values"></a>Codifica/decodifica dei valori restituiti ASN.1

La tabella seguente contiene i valori restituiti che possono essere restituiti dalle funzioni che eseguono la codifica o la decodifica ASN.1 [*(Abstract Syntax Notation One).*](../secgloss/a-gly.md)



| Costante definita           | SMS                                      | Valore esadecimale |
|----------------------------|---------------------------------------------------|-------------------|
| ERRORE \_ CRYPT E \_ ASN1 \_      | AsN.1 Certificate encode/decode return value base (Base del valore restituito del certificato ASN.1) | 0x80093100        |
| CRYPT \_ E \_ ASN1 \_ INTERNAL   | Errore interno di codifica o decodifica ASN.1             | 0x80093101        |
| CRYPT \_ E \_ ASN1 \_ EOD        | ASN.1 fine imprevista dei dati                      | 0x80093102        |
| CRYPT \_ E \_ ASN1 \_ DANNEGGIATO    | Dati danneggiati ASN.1                              | 0x80093103        |
| CRYPT \_ E \_ ASN1 \_ LARGE      | Valore ASN.1 troppo grande                             | 0x80093104        |
| VINCOLO \_ CRYPT E \_ ASN1 \_ | Vincolo ASN.1 violato                         | 0x80093105        |
| MEMORIA \_ CRYPT E \_ ASN1 \_     | MEMORIA INSUFFICIENTE ASN.1                               | 0x80093106        |
| OVERFLOW DI CRYPT \_ E \_ ASN1 \_   | Overflow del buffer ASN.1                             | 0x80093107        |
| CRYPT \_ E \_ ASN1 \_ BADPDU     | Funzione ASN.1 non supportata per questa PDU         | 0x80093108        |
| CRYPT \_ E \_ ASN1 \_ BADARGS    | ASN.1 Argomenti non validi per la chiamata di funzione              | 0x80093109        |
| CRYPT \_ E \_ ASN1 \_ BADREAL    | ASN.1 valore reale non valido                              | 0x8009310A        |
| CRYPT \_ E \_ ASN1 \_ BADTAG     | AsN.1: valore di tag non valido soddisfatto                           | 0x8009310B        |
| SCELTA \_ DI CRYPT E \_ ASN1 \_     | ASN.1 Valore di scelta non valido                            | 0x8009310C        |
| REGOLA \_ CRYPT E \_ ASN1 \_       | Regola di codifica ASN.1 non valida                           | 0x8009310D        |
| CRYPT \_ E \_ ASN1 \_ UTF8       | ASN.1 Unicode non erta (UTF8)                          | 0x8009310E        |
| TIPO PDU CRYPT \_ E \_ ASN1 \_ \_  | AsN.1 tipo di PDU non valido                                | 0x80093133        |
| CRYPT \_ E \_ ASN1 \_ NYI        | ASN.1 non ancora implementato                         | 0x80093134        |
| CRYPT \_ E \_ ASN1 \_ EXTENDED   | AsN.1 ha ignorato le estensioni sconosciute                  | 0x80093201        |
| CRYPT \_ E \_ ASN1 \_ NOEOD      | È prevista la fine dei dati ASN.1                        | 0x80093202        |



 

 

 
